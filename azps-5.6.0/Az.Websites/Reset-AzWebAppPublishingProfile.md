---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 9d3a17280f80ef0376912f806439698f24cdfe25
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008203"
---
# <span data-ttu-id="35f0e-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="35f0e-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="35f0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35f0e-102">SYNOPSIS</span></span>

## <span data-ttu-id="35f0e-103">구문</span><span class="sxs-lookup"><span data-stu-id="35f0e-103">SYNTAX</span></span>

### <span data-ttu-id="35f0e-104">S1</span><span class="sxs-lookup"><span data-stu-id="35f0e-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35f0e-105">S2</span><span class="sxs-lookup"><span data-stu-id="35f0e-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35f0e-106">설명</span><span class="sxs-lookup"><span data-stu-id="35f0e-106">DESCRIPTION</span></span>
<span data-ttu-id="35f0e-107">**Reset-AzWebAppPublishingProfile** cmdlet은 지정된 웹앱에 대한 게시 프로필을 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="35f0e-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="35f0e-108">예제</span><span class="sxs-lookup"><span data-stu-id="35f0e-108">EXAMPLES</span></span>

### <span data-ttu-id="35f0e-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="35f0e-109">Example 1</span></span>

<span data-ttu-id="35f0e-110">다음 예제에서는 리소스 그룹 MyResourceGroup과 연결된 웹앱 IpRule에 대한 게시 프로필을 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="35f0e-110">The following example resets the publishing profile for the Web App IpRule associated with the resource group MyResourceGroup.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Reset-AzWebAppPublishingProfile -Name IpRule -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="35f0e-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="35f0e-111">PARAMETERS</span></span>

### <span data-ttu-id="35f0e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f0e-112">-DefaultProfile</span></span>
<span data-ttu-id="35f0e-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35f0e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35f0e-114">-Name</span><span class="sxs-lookup"><span data-stu-id="35f0e-114">-Name</span></span>
<span data-ttu-id="35f0e-115">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="35f0e-115">WebApp Name</span></span>

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

### <span data-ttu-id="35f0e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35f0e-116">-ResourceGroupName</span></span>
<span data-ttu-id="35f0e-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="35f0e-117">Resource Group Name</span></span>

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

### <span data-ttu-id="35f0e-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="35f0e-118">-WebApp</span></span>
<span data-ttu-id="35f0e-119">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="35f0e-119">WebApp Object</span></span>

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

### <span data-ttu-id="35f0e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f0e-120">CommonParameters</span></span>
<span data-ttu-id="35f0e-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="35f0e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f0e-122">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="35f0e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f0e-123">입력</span><span class="sxs-lookup"><span data-stu-id="35f0e-123">INPUTS</span></span>

### <span data-ttu-id="35f0e-124">System.String</span><span class="sxs-lookup"><span data-stu-id="35f0e-124">System.String</span></span>

### <span data-ttu-id="35f0e-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="35f0e-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="35f0e-126">출력</span><span class="sxs-lookup"><span data-stu-id="35f0e-126">OUTPUTS</span></span>

### <span data-ttu-id="35f0e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="35f0e-127">System.String</span></span>

## <span data-ttu-id="35f0e-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="35f0e-128">NOTES</span></span>

## <span data-ttu-id="35f0e-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35f0e-129">RELATED LINKS</span></span>
