# JDA-shutdown-error-Help-please
I do not have much experience with java but I´m trying to code a Discord Bot. My problem is that i tried to get a shutdown method which shut the Bot down when i type !shutdown in the Discord chat, but it´s not working and i can´t find any solution on Google. Thank you for your help


package de.InfinitySplashes.listener;

import javax.annotation.Nonnull;

import de.InfinitySplashes.shutdown;
import de.InfinitySplashes.constants.constants;
import net.dv8tion.jda.api.entities.Guild;
import net.dv8tion.jda.api.entities.Message;
import net.dv8tion.jda.api.entities.User;
import net.dv8tion.jda.api.events.ShutdownEvent;
import net.dv8tion.jda.api.events.message.MessageReceivedEvent;
import net.dv8tion.jda.api.events.message.guild.GuildMessageReceivedEvent;
import net.dv8tion.jda.api.hooks.ListenerAdapter;

public class Shutdown extends ListenerAdapter{
	public Shutdown() {
		
		
	}

    public void onGuildMessageReceived(@Nonnull GuildMessageReceivedEvent event) {
    	

		Message message = event.getMessage();
		
		String msg = message.getContentDisplay();	
    
		System.out.println("Phase 1");
		
	
	if(msg.contains("!shutdown")) {
		
		boolean shutd = true;
		System.out.println("Phase 2");
		if(shutd = true) {
			
		event.getJDA().shutdownNow();
			System.out.println("shutting down");
		}
	}
}
	
}
