---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: 85a5c38038116d89e7cab1e6efe2718d4c5a697b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989151"
---
# <span data-ttu-id="fe47f-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="fe47f-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="fe47f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe47f-102">SYNOPSIS</span></span>
<span data-ttu-id="fe47f-103">정책 메타데이터 리소스 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fe47f-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="fe47f-104">구문</span><span class="sxs-lookup"><span data-stu-id="fe47f-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe47f-105">설명</span><span class="sxs-lookup"><span data-stu-id="fe47f-105">DESCRIPTION</span></span>
<span data-ttu-id="fe47f-106">**Get-AzPolicyRemediation** cmdlet은 모든 정책 메타데이터 리소스 또는 특정 정책 메타데이터 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fe47f-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="fe47f-107">예제</span><span class="sxs-lookup"><span data-stu-id="fe47f-107">EXAMPLES</span></span>

### <span data-ttu-id="fe47f-108">예제 1: 모든 정책 메타데이터 리소스 사용</span><span class="sxs-lookup"><span data-stu-id="fe47f-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="fe47f-109">이 명령은 모든 정책 메타데이터 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fe47f-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="fe47f-110">예제 2: 10개 정책 메타데이터 리소스 컬렉션을 수집합니다.</span><span class="sxs-lookup"><span data-stu-id="fe47f-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="fe47f-111">이 명령은 10개 정책 메타데이터 리소스의 컬렉션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fe47f-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="fe47f-112">예제 3: 'ACF1348' 이름으로 단일 정책 메타데이터 리소스 얻기</span><span class="sxs-lookup"><span data-stu-id="fe47f-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="fe47f-113">이 명령은 'ACF1348'으로 단일 정책 메타데이터 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fe47f-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="fe47f-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fe47f-114">PARAMETERS</span></span>

### <span data-ttu-id="fe47f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe47f-115">-DefaultProfile</span></span>
<span data-ttu-id="fe47f-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fe47f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe47f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fe47f-117">-Name</span></span>
<span data-ttu-id="fe47f-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fe47f-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe47f-119">-Top</span><span class="sxs-lookup"><span data-stu-id="fe47f-119">-Top</span></span>
<span data-ttu-id="fe47f-120">반환할 정책 메타데이터 리소스의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fe47f-120">Maximum number of policy metadata resources to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe47f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe47f-121">CommonParameters</span></span>
<span data-ttu-id="fe47f-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fe47f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe47f-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe47f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe47f-124">입력</span><span class="sxs-lookup"><span data-stu-id="fe47f-124">INPUTS</span></span>

### <span data-ttu-id="fe47f-125">System.String</span><span class="sxs-lookup"><span data-stu-id="fe47f-125">System.String</span></span>

## <span data-ttu-id="fe47f-126">출력</span><span class="sxs-lookup"><span data-stu-id="fe47f-126">OUTPUTS</span></span>

### <span data-ttu-id="fe47f-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="fe47f-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="fe47f-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fe47f-128">NOTES</span></span>

## <span data-ttu-id="fe47f-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe47f-129">RELATED LINKS</span></span>
