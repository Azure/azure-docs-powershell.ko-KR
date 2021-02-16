---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4bd0e45df7f1c5c98b61f7f490a59a4c305c2c21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207485"
---
# <span data-ttu-id="303cb-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="303cb-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="303cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="303cb-102">SYNOPSIS</span></span>
<span data-ttu-id="303cb-103">Azure 웹앱 슬롯을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="303cb-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="303cb-104">구문</span><span class="sxs-lookup"><span data-stu-id="303cb-104">SYNTAX</span></span>

### <span data-ttu-id="303cb-105">S1</span><span class="sxs-lookup"><span data-stu-id="303cb-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="303cb-106">S2</span><span class="sxs-lookup"><span data-stu-id="303cb-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="303cb-107">설명</span><span class="sxs-lookup"><span data-stu-id="303cb-107">DESCRIPTION</span></span>
<span data-ttu-id="303cb-108">**Get-AzWebAppSlot** cmdlet은 Azure 웹앱 슬롯에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="303cb-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="303cb-109">예제</span><span class="sxs-lookup"><span data-stu-id="303cb-109">EXAMPLES</span></span>

### <span data-ttu-id="303cb-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="303cb-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="303cb-111">이 명령은 리소스 그룹 Default-Web-WestUS에 속하는 WebAppStandard라는 웹앱에서 Slot001이라는 슬롯을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="303cb-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="303cb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="303cb-112">PARAMETERS</span></span>

### <span data-ttu-id="303cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="303cb-113">-DefaultProfile</span></span>
<span data-ttu-id="303cb-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="303cb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="303cb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="303cb-115">-Name</span></span>
<span data-ttu-id="303cb-116">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="303cb-116">WebApp Name</span></span>

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

### <span data-ttu-id="303cb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="303cb-117">-ResourceGroupName</span></span>
<span data-ttu-id="303cb-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="303cb-118">Resource Group Name</span></span>

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

### <span data-ttu-id="303cb-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="303cb-119">-Slot</span></span>
<span data-ttu-id="303cb-120">WebApp 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="303cb-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="303cb-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="303cb-121">-WebApp</span></span>
<span data-ttu-id="303cb-122">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="303cb-122">WebApp Object</span></span>

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

### <span data-ttu-id="303cb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="303cb-123">CommonParameters</span></span>
<span data-ttu-id="303cb-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="303cb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="303cb-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="303cb-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="303cb-126">입력</span><span class="sxs-lookup"><span data-stu-id="303cb-126">INPUTS</span></span>

### <span data-ttu-id="303cb-127">System.String</span><span class="sxs-lookup"><span data-stu-id="303cb-127">System.String</span></span>

### <span data-ttu-id="303cb-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="303cb-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="303cb-129">출력</span><span class="sxs-lookup"><span data-stu-id="303cb-129">OUTPUTS</span></span>

### <span data-ttu-id="303cb-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="303cb-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="303cb-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="303cb-131">NOTES</span></span>

## <span data-ttu-id="303cb-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="303cb-132">RELATED LINKS</span></span>

[<span data-ttu-id="303cb-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="303cb-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="303cb-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="303cb-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="303cb-135">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="303cb-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="303cb-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="303cb-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="303cb-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="303cb-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="303cb-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="303cb-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="303cb-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="303cb-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
