---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: 4425c344fb0c9e0e3441c172915be11002ee8b1b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207432"
---
# <span data-ttu-id="63a44-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63a44-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="63a44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63a44-102">SYNOPSIS</span></span>
<span data-ttu-id="63a44-103">Azure 웹앱 슬롯을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="63a44-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="63a44-104">구문</span><span class="sxs-lookup"><span data-stu-id="63a44-104">SYNTAX</span></span>

### <span data-ttu-id="63a44-105">S1</span><span class="sxs-lookup"><span data-stu-id="63a44-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63a44-106">S2</span><span class="sxs-lookup"><span data-stu-id="63a44-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63a44-107">설명</span><span class="sxs-lookup"><span data-stu-id="63a44-107">DESCRIPTION</span></span>
<span data-ttu-id="63a44-108">**Start-AzWebAppSlot** cmdlet은 Azure 웹앱 슬롯을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="63a44-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="63a44-109">예제</span><span class="sxs-lookup"><span data-stu-id="63a44-109">EXAMPLES</span></span>

### <span data-ttu-id="63a44-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="63a44-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="63a44-111">이 명령은 Default-Web-WestUS라는 리소스 그룹에 속하는 ContosoWebApp이라는 웹앱과 관련한 Slot001 슬롯을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="63a44-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="63a44-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63a44-112">PARAMETERS</span></span>

### <span data-ttu-id="63a44-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63a44-113">-DefaultProfile</span></span>
<span data-ttu-id="63a44-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="63a44-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63a44-115">-Name</span><span class="sxs-lookup"><span data-stu-id="63a44-115">-Name</span></span>
<span data-ttu-id="63a44-116">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="63a44-116">WebApp Name</span></span>

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

### <span data-ttu-id="63a44-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63a44-117">-ResourceGroupName</span></span>
<span data-ttu-id="63a44-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="63a44-118">Resource Group Name</span></span>

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

### <span data-ttu-id="63a44-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="63a44-119">-Slot</span></span>
<span data-ttu-id="63a44-120">WebApp 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="63a44-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="63a44-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="63a44-121">-WebApp</span></span>
<span data-ttu-id="63a44-122">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="63a44-122">WebApp Object</span></span>

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

### <span data-ttu-id="63a44-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63a44-123">CommonParameters</span></span>
<span data-ttu-id="63a44-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="63a44-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63a44-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="63a44-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63a44-126">입력</span><span class="sxs-lookup"><span data-stu-id="63a44-126">INPUTS</span></span>

### <span data-ttu-id="63a44-127">System.String</span><span class="sxs-lookup"><span data-stu-id="63a44-127">System.String</span></span>

### <span data-ttu-id="63a44-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="63a44-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="63a44-129">출력</span><span class="sxs-lookup"><span data-stu-id="63a44-129">OUTPUTS</span></span>

### <span data-ttu-id="63a44-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="63a44-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="63a44-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="63a44-131">NOTES</span></span>

## <span data-ttu-id="63a44-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63a44-132">RELATED LINKS</span></span>

[<span data-ttu-id="63a44-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63a44-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="63a44-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63a44-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="63a44-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63a44-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="63a44-136">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63a44-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="63a44-137">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63a44-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="63a44-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="63a44-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="63a44-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="63a44-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
