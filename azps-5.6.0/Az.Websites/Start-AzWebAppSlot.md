---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: c65eac94a9c44b3b7272116bc0e0757291b121b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011072"
---
# <span data-ttu-id="16271-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16271-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="16271-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16271-102">SYNOPSIS</span></span>
<span data-ttu-id="16271-103">Azure Web App 슬롯을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="16271-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="16271-104">구문</span><span class="sxs-lookup"><span data-stu-id="16271-104">SYNTAX</span></span>

### <span data-ttu-id="16271-105">S1</span><span class="sxs-lookup"><span data-stu-id="16271-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16271-106">S2</span><span class="sxs-lookup"><span data-stu-id="16271-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16271-107">설명</span><span class="sxs-lookup"><span data-stu-id="16271-107">DESCRIPTION</span></span>
<span data-ttu-id="16271-108">**Start-AzWebAppSlot cmdlet은** Azure Web App Slot을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="16271-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="16271-109">예제</span><span class="sxs-lookup"><span data-stu-id="16271-109">EXAMPLES</span></span>

### <span data-ttu-id="16271-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="16271-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="16271-111">이 명령은 Default-Web-WestUS라는 리소스 그룹에 속하는 ContosoWebApp이라는 웹앱에 대한 Slot001이라는 슬롯을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="16271-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="16271-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="16271-112">PARAMETERS</span></span>

### <span data-ttu-id="16271-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16271-113">-DefaultProfile</span></span>
<span data-ttu-id="16271-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16271-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16271-115">-Name</span><span class="sxs-lookup"><span data-stu-id="16271-115">-Name</span></span>
<span data-ttu-id="16271-116">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="16271-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16271-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16271-117">-ResourceGroupName</span></span>
<span data-ttu-id="16271-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="16271-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16271-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="16271-119">-Slot</span></span>
<span data-ttu-id="16271-120">WebApp 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="16271-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16271-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="16271-121">-WebApp</span></span>
<span data-ttu-id="16271-122">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="16271-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16271-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16271-123">CommonParameters</span></span>
<span data-ttu-id="16271-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="16271-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16271-125">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="16271-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16271-126">입력</span><span class="sxs-lookup"><span data-stu-id="16271-126">INPUTS</span></span>

### <span data-ttu-id="16271-127">System.String</span><span class="sxs-lookup"><span data-stu-id="16271-127">System.String</span></span>

### <span data-ttu-id="16271-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="16271-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="16271-129">출력</span><span class="sxs-lookup"><span data-stu-id="16271-129">OUTPUTS</span></span>

### <span data-ttu-id="16271-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="16271-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="16271-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="16271-131">NOTES</span></span>

## <span data-ttu-id="16271-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16271-132">RELATED LINKS</span></span>

[<span data-ttu-id="16271-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16271-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="16271-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16271-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="16271-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16271-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="16271-136">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16271-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="16271-137">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16271-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="16271-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16271-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="16271-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="16271-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
