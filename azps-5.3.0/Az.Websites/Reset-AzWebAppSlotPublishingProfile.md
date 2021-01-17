---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 840e0bb2bfa10a89a5ba963e83ab434e795b3dd4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491427"
---
# <span data-ttu-id="a78f0-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="a78f0-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="a78f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a78f0-102">SYNOPSIS</span></span>

## <span data-ttu-id="a78f0-103">구문</span><span class="sxs-lookup"><span data-stu-id="a78f0-103">SYNTAX</span></span>

### <span data-ttu-id="a78f0-104">S1</span><span class="sxs-lookup"><span data-stu-id="a78f0-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a78f0-105">S2</span><span class="sxs-lookup"><span data-stu-id="a78f0-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a78f0-106">설명</span><span class="sxs-lookup"><span data-stu-id="a78f0-106">DESCRIPTION</span></span>
<span data-ttu-id="a78f0-107">**Reset-AzWebAppSlotPublishingProfile** cmdlet은 지정된 웹앱 슬롯에 대한 게시 프로필을 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a78f0-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="a78f0-108">예제</span><span class="sxs-lookup"><span data-stu-id="a78f0-108">EXAMPLES</span></span>

### <span data-ttu-id="a78f0-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="a78f0-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="a78f0-110">이 명령은 리소스 그룹 Default-Web-WestUS와 연결된 웹앱 ContosoWebApp에 대해 slot001이라는 슬롯에 대한 게시 프로필을 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a78f0-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a78f0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a78f0-111">PARAMETERS</span></span>

### <span data-ttu-id="a78f0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a78f0-112">-DefaultProfile</span></span>
<span data-ttu-id="a78f0-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a78f0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a78f0-114">-Name</span><span class="sxs-lookup"><span data-stu-id="a78f0-114">-Name</span></span>
<span data-ttu-id="a78f0-115">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="a78f0-115">WebApp Name</span></span>

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

### <span data-ttu-id="a78f0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a78f0-116">-ResourceGroupName</span></span>
<span data-ttu-id="a78f0-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a78f0-117">Resource Group Name</span></span>

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

### <span data-ttu-id="a78f0-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="a78f0-118">-Slot</span></span>
<span data-ttu-id="a78f0-119">WebApp 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="a78f0-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="a78f0-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a78f0-120">-WebApp</span></span>
<span data-ttu-id="a78f0-121">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="a78f0-121">WebApp Object</span></span>

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

### <span data-ttu-id="a78f0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a78f0-122">CommonParameters</span></span>
<span data-ttu-id="a78f0-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a78f0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a78f0-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a78f0-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a78f0-125">입력</span><span class="sxs-lookup"><span data-stu-id="a78f0-125">INPUTS</span></span>

### <span data-ttu-id="a78f0-126">System.String</span><span class="sxs-lookup"><span data-stu-id="a78f0-126">System.String</span></span>

### <span data-ttu-id="a78f0-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="a78f0-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a78f0-128">출력</span><span class="sxs-lookup"><span data-stu-id="a78f0-128">OUTPUTS</span></span>

### <span data-ttu-id="a78f0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a78f0-129">System.String</span></span>

## <span data-ttu-id="a78f0-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a78f0-130">NOTES</span></span>

## <span data-ttu-id="a78f0-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a78f0-131">RELATED LINKS</span></span>
