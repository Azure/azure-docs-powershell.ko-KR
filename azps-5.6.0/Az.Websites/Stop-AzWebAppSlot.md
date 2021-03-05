---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/powershell/module/az.websites/stop-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: 1be0602fc139c5630591dea1e7aa35eaaf27a714
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011003"
---
# <span data-ttu-id="27d8f-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="27d8f-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="27d8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="27d8f-103">Azure Web App 슬롯을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="27d8f-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="27d8f-104">구문</span><span class="sxs-lookup"><span data-stu-id="27d8f-104">SYNTAX</span></span>

### <span data-ttu-id="27d8f-105">S1</span><span class="sxs-lookup"><span data-stu-id="27d8f-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27d8f-106">S2</span><span class="sxs-lookup"><span data-stu-id="27d8f-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27d8f-107">설명</span><span class="sxs-lookup"><span data-stu-id="27d8f-107">DESCRIPTION</span></span>
<span data-ttu-id="27d8f-108">**Stop-AzWebAppSlot cmdlet은** Azure Web App Slot을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="27d8f-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="27d8f-109">예제</span><span class="sxs-lookup"><span data-stu-id="27d8f-109">EXAMPLES</span></span>

### <span data-ttu-id="27d8f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="27d8f-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="27d8f-111">이 명령은 Default-Web-WestUS라는 리소스 그룹에 속하는 ContosoWebApp이라는 웹앱에 대한 슬롯 슬롯001을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="27d8f-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="27d8f-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="27d8f-112">PARAMETERS</span></span>

### <span data-ttu-id="27d8f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27d8f-113">-DefaultProfile</span></span>
<span data-ttu-id="27d8f-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27d8f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27d8f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="27d8f-115">-Name</span></span>
<span data-ttu-id="27d8f-116">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="27d8f-116">WebApp Name</span></span>

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

### <span data-ttu-id="27d8f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27d8f-117">-ResourceGroupName</span></span>
<span data-ttu-id="27d8f-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="27d8f-118">Resource Group Name</span></span>

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

### <span data-ttu-id="27d8f-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="27d8f-119">-Slot</span></span>
<span data-ttu-id="27d8f-120">WebApp 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="27d8f-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="27d8f-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="27d8f-121">-WebApp</span></span>
<span data-ttu-id="27d8f-122">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="27d8f-122">WebApp Object</span></span>

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

### <span data-ttu-id="27d8f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27d8f-123">CommonParameters</span></span>
<span data-ttu-id="27d8f-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="27d8f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27d8f-125">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="27d8f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27d8f-126">입력</span><span class="sxs-lookup"><span data-stu-id="27d8f-126">INPUTS</span></span>

### <span data-ttu-id="27d8f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="27d8f-127">System.String</span></span>

### <span data-ttu-id="27d8f-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="27d8f-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="27d8f-129">출력</span><span class="sxs-lookup"><span data-stu-id="27d8f-129">OUTPUTS</span></span>

### <span data-ttu-id="27d8f-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="27d8f-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="27d8f-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="27d8f-131">NOTES</span></span>

## <span data-ttu-id="27d8f-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27d8f-132">RELATED LINKS</span></span>
