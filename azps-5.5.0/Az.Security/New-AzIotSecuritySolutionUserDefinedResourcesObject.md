---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionUserDefinedResourcesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
ms.openlocfilehash: e824c32ae2ae4f28972cdac9446eeeae6e410c75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208312"
---
# <span data-ttu-id="762ad-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span><span class="sxs-lookup"><span data-stu-id="762ad-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span></span>

## <span data-ttu-id="762ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="762ad-102">SYNOPSIS</span></span>
<span data-ttu-id="762ad-103">iot 보안 솔루션에 대한 새 사용자 정의 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="762ad-103">Create new user defined resources for iot security solution</span></span>

## <span data-ttu-id="762ad-104">구문</span><span class="sxs-lookup"><span data-stu-id="762ad-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionUserDefinedResourcesObject -Query <String> -QuerySubscriptionList <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="762ad-105">설명</span><span class="sxs-lookup"><span data-stu-id="762ad-105">DESCRIPTION</span></span>
<span data-ttu-id="762ad-106">AzIotSecuritySolutionUserDefinedResourcesObject cmdlet은 iot 보안 솔루션에 대한 새 사용자 정의 리소스 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="762ad-106">The AzIotSecuritySolutionUserDefinedResourcesObject cmdlet creates a new user defined resources object for the iot security solution.</span></span>

## <span data-ttu-id="762ad-107">예제</span><span class="sxs-lookup"><span data-stu-id="762ad-107">EXAMPLES</span></span>

### <span data-ttu-id="762ad-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="762ad-108">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")

Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
QuerySubscriptions: ["XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX"]
```

<span data-ttu-id="762ad-109">새 사용자 정의 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="762ad-109">Create new user defined resources</span></span>

## <span data-ttu-id="762ad-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="762ad-110">PARAMETERS</span></span>

### <span data-ttu-id="762ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="762ad-111">-DefaultProfile</span></span>
<span data-ttu-id="762ad-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="762ad-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="762ad-113">-Query</span><span class="sxs-lookup"><span data-stu-id="762ad-113">-Query</span></span>
<span data-ttu-id="762ad-114">쿼리.</span><span class="sxs-lookup"><span data-stu-id="762ad-114">Query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762ad-115">-QuerySubscriptionList</span><span class="sxs-lookup"><span data-stu-id="762ad-115">-QuerySubscriptionList</span></span>
<span data-ttu-id="762ad-116">구독을 쿼리합니다.</span><span class="sxs-lookup"><span data-stu-id="762ad-116">Query subscriptions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762ad-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="762ad-117">CommonParameters</span></span>
<span data-ttu-id="762ad-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="762ad-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="762ad-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="762ad-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="762ad-120">입력</span><span class="sxs-lookup"><span data-stu-id="762ad-120">INPUTS</span></span>

### <span data-ttu-id="762ad-121">없음</span><span class="sxs-lookup"><span data-stu-id="762ad-121">None</span></span>

## <span data-ttu-id="762ad-122">출력</span><span class="sxs-lookup"><span data-stu-id="762ad-122">OUTPUTS</span></span>

### <span data-ttu-id="762ad-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="762ad-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

## <span data-ttu-id="762ad-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="762ad-124">NOTES</span></span>

## <span data-ttu-id="762ad-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="762ad-125">RELATED LINKS</span></span>
