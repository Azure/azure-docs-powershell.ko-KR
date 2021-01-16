---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 81005ceac6bfa3c258a147f3fbef168e95c302cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326059"
---
# <span data-ttu-id="f1e31-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="f1e31-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="f1e31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1e31-102">SYNOPSIS</span></span>

## <span data-ttu-id="f1e31-103">구문</span><span class="sxs-lookup"><span data-stu-id="f1e31-103">SYNTAX</span></span>

### <span data-ttu-id="f1e31-104">S1</span><span class="sxs-lookup"><span data-stu-id="f1e31-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1e31-105">S2</span><span class="sxs-lookup"><span data-stu-id="f1e31-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1e31-106">설명</span><span class="sxs-lookup"><span data-stu-id="f1e31-106">DESCRIPTION</span></span>
<span data-ttu-id="f1e31-107">**Reset-AzWebAppPublishingProfile** cmdlet은 지정된 웹앱에 대한 게시 프로필을 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f1e31-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="f1e31-108">예제</span><span class="sxs-lookup"><span data-stu-id="f1e31-108">EXAMPLES</span></span>

### <span data-ttu-id="f1e31-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="f1e31-109">Example 1</span></span>

<span data-ttu-id="f1e31-110">다음 예제에서는 리소스 그룹 MyResourceGroup과 연결된 웹앱 IpRule에 대한 게시 프로필을 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f1e31-110">The following example resets the publishing profile for the Web App IpRule associated with the resource group MyResourceGroup.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Reset-AzWebAppPublishingProfile -Name IpRule -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="f1e31-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1e31-111">PARAMETERS</span></span>

### <span data-ttu-id="f1e31-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e31-112">-DefaultProfile</span></span>
<span data-ttu-id="f1e31-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1e31-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1e31-114">-Name</span><span class="sxs-lookup"><span data-stu-id="f1e31-114">-Name</span></span>
<span data-ttu-id="f1e31-115">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="f1e31-115">WebApp Name</span></span>

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

### <span data-ttu-id="f1e31-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1e31-116">-ResourceGroupName</span></span>
<span data-ttu-id="f1e31-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f1e31-117">Resource Group Name</span></span>

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

### <span data-ttu-id="f1e31-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f1e31-118">-WebApp</span></span>
<span data-ttu-id="f1e31-119">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="f1e31-119">WebApp Object</span></span>

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

### <span data-ttu-id="f1e31-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e31-120">CommonParameters</span></span>
<span data-ttu-id="f1e31-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f1e31-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e31-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f1e31-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e31-123">입력</span><span class="sxs-lookup"><span data-stu-id="f1e31-123">INPUTS</span></span>

### <span data-ttu-id="f1e31-124">System.String</span><span class="sxs-lookup"><span data-stu-id="f1e31-124">System.String</span></span>

### <span data-ttu-id="f1e31-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f1e31-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f1e31-126">출력</span><span class="sxs-lookup"><span data-stu-id="f1e31-126">OUTPUTS</span></span>

### <span data-ttu-id="f1e31-127">System.String</span><span class="sxs-lookup"><span data-stu-id="f1e31-127">System.String</span></span>

## <span data-ttu-id="f1e31-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f1e31-128">NOTES</span></span>

## <span data-ttu-id="f1e31-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1e31-129">RELATED LINKS</span></span>
