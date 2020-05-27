---
title: Azure PowerShell을 사용하여 Azure 구독 관리
description: Azure PowerShell을 사용하여 Azure 구독 관리
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 757d908de765d60428a3df17ba7c827f50360f3b
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83387890"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="09552-103">여러 Azure 구독 관리</span><span class="sxs-lookup"><span data-stu-id="09552-103">Manage multiple Azure subscriptions</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="09552-104">Azure를 처음 접하는 분들은 아마도 구독을 하나만 갖고 계실 것입니다.</span><span class="sxs-lookup"><span data-stu-id="09552-104">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="09552-105">하지만 한동안 Azure를 사용해 오신 분들 중에는 Azure 구독을 여러 개 만든 분도 있을 것입니다.</span><span class="sxs-lookup"><span data-stu-id="09552-105">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="09552-106">특정 구독에 대해 명령을 실행하도록 Azure PowerShell을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09552-106">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="09552-107">계정의 모든 구독 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="09552-107">Get a list of all subscriptions in your account.</span></span>

    ```azurepowershell-interactive
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My DevTest Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

2. <span data-ttu-id="09552-108">기본 구독을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="09552-108">Set the default.</span></span>

    ```azurepowershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. <span data-ttu-id="09552-109">`Get-AzureRmContext` cmdlet을 실행하여 변경 내용을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="09552-109">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

    ```azurepowershell-interactive
    Get-AzureRmContext
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

<span data-ttu-id="09552-110">기본 구독을 설정한 이후부터는 모든 Azure PowerShell 명령이 기본 구독에 대해 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="09552-110">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
