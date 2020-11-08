---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216032"
---
# <span data-ttu-id="e2d9b-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="e2d9b-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="e2d9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="e2d9b-103">정책 메타 데이터 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="e2d9b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2d9b-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2d9b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e2d9b-105">DESCRIPTION</span></span>
<span data-ttu-id="e2d9b-106">**Get-AzPolicyRemediation** cmdlet은 모든 정책 메타 데이터 리소스 또는 특정 정책 메타 데이터 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="e2d9b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e2d9b-107">EXAMPLES</span></span>

### <span data-ttu-id="e2d9b-108">예제 1: 모든 정책 메타 데이터 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="e2d9b-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="e2d9b-109">이 명령은 모든 정책 메타 데이터 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="e2d9b-110">예제 2:10 개의 정책 메타 데이터 리소스 컬렉션 가져오기</span><span class="sxs-lookup"><span data-stu-id="e2d9b-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="e2d9b-111">이 명령은 10 개의 정책 메타 데이터 리소스의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="e2d9b-112">예제 3: 이름이 ' ACF1348 ' 인 단일 정책 메타 데이터 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="e2d9b-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="e2d9b-113">이 명령은 이름이 ' ACF1348 ' 인 단일 정책 메타 데이터 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="e2d9b-114">변수</span><span class="sxs-lookup"><span data-stu-id="e2d9b-114">PARAMETERS</span></span>

### <span data-ttu-id="e2d9b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2d9b-115">-DefaultProfile</span></span>
<span data-ttu-id="e2d9b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2d9b-117">-이름</span><span class="sxs-lookup"><span data-stu-id="e2d9b-117">-Name</span></span>
<span data-ttu-id="e2d9b-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-118">Resource name.</span></span>

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

### <span data-ttu-id="e2d9b-119">-위쪽</span><span class="sxs-lookup"><span data-stu-id="e2d9b-119">-Top</span></span>
<span data-ttu-id="e2d9b-120">반환할 정책 메타 데이터 리소스의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-120">Maximum number of policy metadata resources to return.</span></span>

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

### <span data-ttu-id="e2d9b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2d9b-121">CommonParameters</span></span>
<span data-ttu-id="e2d9b-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2d9b-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2d9b-124">입력</span><span class="sxs-lookup"><span data-stu-id="e2d9b-124">INPUTS</span></span>

### <span data-ttu-id="e2d9b-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e2d9b-125">System.String</span></span>

## <span data-ttu-id="e2d9b-126">출력</span><span class="sxs-lookup"><span data-stu-id="e2d9b-126">OUTPUTS</span></span>

### <span data-ttu-id="e2d9b-127">PSPolicyMetadata-PolicyInsights. 모델.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="e2d9b-128">상속자</span><span class="sxs-lookup"><span data-stu-id="e2d9b-128">NOTES</span></span>

## <span data-ttu-id="e2d9b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2d9b-129">RELATED LINKS</span></span>
