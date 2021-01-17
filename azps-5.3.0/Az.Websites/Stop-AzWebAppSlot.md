---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: eba40b4c372fd900ac42bead0e2c0b39305c91cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491395"
---
# <span data-ttu-id="e787b-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e787b-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="e787b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e787b-102">SYNOPSIS</span></span>
<span data-ttu-id="e787b-103">Azure 웹앱 슬롯을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="e787b-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="e787b-104">구문</span><span class="sxs-lookup"><span data-stu-id="e787b-104">SYNTAX</span></span>

### <span data-ttu-id="e787b-105">S1</span><span class="sxs-lookup"><span data-stu-id="e787b-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e787b-106">S2</span><span class="sxs-lookup"><span data-stu-id="e787b-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e787b-107">설명</span><span class="sxs-lookup"><span data-stu-id="e787b-107">DESCRIPTION</span></span>
<span data-ttu-id="e787b-108">**Stop-AzWebAppSlot** cmdlet은 Azure 웹앱 슬롯을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="e787b-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="e787b-109">예제</span><span class="sxs-lookup"><span data-stu-id="e787b-109">EXAMPLES</span></span>

### <span data-ttu-id="e787b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e787b-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="e787b-111">이 명령은 Default-Web-WestUS라는 리소스 그룹에 속하는 ContosoWebApp이라는 웹앱과 관련한 Slot001 슬롯을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="e787b-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="e787b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e787b-112">PARAMETERS</span></span>

### <span data-ttu-id="e787b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e787b-113">-DefaultProfile</span></span>
<span data-ttu-id="e787b-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e787b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e787b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e787b-115">-Name</span></span>
<span data-ttu-id="e787b-116">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="e787b-116">WebApp Name</span></span>

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

### <span data-ttu-id="e787b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e787b-117">-ResourceGroupName</span></span>
<span data-ttu-id="e787b-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e787b-118">Resource Group Name</span></span>

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

### <span data-ttu-id="e787b-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="e787b-119">-Slot</span></span>
<span data-ttu-id="e787b-120">WebApp 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="e787b-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="e787b-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e787b-121">-WebApp</span></span>
<span data-ttu-id="e787b-122">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="e787b-122">WebApp Object</span></span>

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

### <span data-ttu-id="e787b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e787b-123">CommonParameters</span></span>
<span data-ttu-id="e787b-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e787b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e787b-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e787b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e787b-126">입력</span><span class="sxs-lookup"><span data-stu-id="e787b-126">INPUTS</span></span>

### <span data-ttu-id="e787b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="e787b-127">System.String</span></span>

### <span data-ttu-id="e787b-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e787b-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e787b-129">출력</span><span class="sxs-lookup"><span data-stu-id="e787b-129">OUTPUTS</span></span>

### <span data-ttu-id="e787b-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e787b-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e787b-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e787b-131">NOTES</span></span>

## <span data-ttu-id="e787b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e787b-132">RELATED LINKS</span></span>
