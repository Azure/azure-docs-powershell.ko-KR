---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 2f57ba64880f40a411ccac3263fa973815c685f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014475"
---
# <span data-ttu-id="d56fb-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d56fb-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="d56fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d56fb-102">SYNOPSIS</span></span>
<span data-ttu-id="d56fb-103">Azure Web App 슬롯을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d56fb-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="d56fb-104">구문</span><span class="sxs-lookup"><span data-stu-id="d56fb-104">SYNTAX</span></span>

### <span data-ttu-id="d56fb-105">S1</span><span class="sxs-lookup"><span data-stu-id="d56fb-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d56fb-106">S2</span><span class="sxs-lookup"><span data-stu-id="d56fb-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d56fb-107">설명</span><span class="sxs-lookup"><span data-stu-id="d56fb-107">DESCRIPTION</span></span>
<span data-ttu-id="d56fb-108">**Get-AzWebAppSlot cmdlet은** Azure Web App Slot에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d56fb-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="d56fb-109">예제</span><span class="sxs-lookup"><span data-stu-id="d56fb-109">EXAMPLES</span></span>

### <span data-ttu-id="d56fb-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d56fb-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="d56fb-111">이 명령은 Resource Group Default-Web-WestUS에 속하는 WebAppStandard라는 웹앱에서 Slot001이라는 슬롯을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d56fb-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d56fb-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d56fb-112">PARAMETERS</span></span>

### <span data-ttu-id="d56fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d56fb-113">-DefaultProfile</span></span>
<span data-ttu-id="d56fb-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d56fb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d56fb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d56fb-115">-Name</span></span>
<span data-ttu-id="d56fb-116">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="d56fb-116">WebApp Name</span></span>

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

### <span data-ttu-id="d56fb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d56fb-117">-ResourceGroupName</span></span>
<span data-ttu-id="d56fb-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d56fb-118">Resource Group Name</span></span>

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

### <span data-ttu-id="d56fb-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="d56fb-119">-Slot</span></span>
<span data-ttu-id="d56fb-120">WebApp 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="d56fb-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56fb-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d56fb-121">-WebApp</span></span>
<span data-ttu-id="d56fb-122">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="d56fb-122">WebApp Object</span></span>

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

### <span data-ttu-id="d56fb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d56fb-123">CommonParameters</span></span>
<span data-ttu-id="d56fb-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d56fb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d56fb-125">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d56fb-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d56fb-126">입력</span><span class="sxs-lookup"><span data-stu-id="d56fb-126">INPUTS</span></span>

### <span data-ttu-id="d56fb-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d56fb-127">System.String</span></span>

### <span data-ttu-id="d56fb-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="d56fb-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d56fb-129">출력</span><span class="sxs-lookup"><span data-stu-id="d56fb-129">OUTPUTS</span></span>

### <span data-ttu-id="d56fb-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="d56fb-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d56fb-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d56fb-131">NOTES</span></span>

## <span data-ttu-id="d56fb-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d56fb-132">RELATED LINKS</span></span>

[<span data-ttu-id="d56fb-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d56fb-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="d56fb-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d56fb-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="d56fb-135">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d56fb-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="d56fb-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d56fb-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="d56fb-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d56fb-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="d56fb-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d56fb-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="d56fb-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d56fb-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
