---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: cd173d17b0867fb5c635b77ee6c72847dc845cb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042971"
---
# <span data-ttu-id="f2680-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="f2680-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="f2680-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2680-102">SYNOPSIS</span></span>
<span data-ttu-id="f2680-103">구독 또는 리소스 그룹의 모든 리소스에 대해 정책 준수 평가를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="f2680-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="f2680-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2680-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2680-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f2680-105">DESCRIPTION</span></span>
<span data-ttu-id="f2680-106">**AzPolicyComplianceScan** cmdlet은 구독 또는 리소스 그룹에 대 한 정책 준수 평가를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2680-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="f2680-107">해당 범위 내의 모든 리소스에는 할당 된 모든 정책에 대해 해당 준수 상태가 평가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2680-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="f2680-108">예제의</span><span class="sxs-lookup"><span data-stu-id="f2680-108">EXAMPLES</span></span>

### <span data-ttu-id="f2680-109">예제 1: 구독 범위에서 준수 검사 시작</span><span class="sxs-lookup"><span data-stu-id="f2680-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="f2680-110">이 명령은 활성 구독에 대 한 정책 준수 평가를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2680-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="f2680-111">예제 2: 리소스 그룹 범위에서 준수 검사 시작</span><span class="sxs-lookup"><span data-stu-id="f2680-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="f2680-112">이 명령은 활성 구독의 "myRG" 리소스 그룹에 대 한 정책 준수 평가를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2680-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="f2680-113">예제 3: 준수 검사 시작 및 백그라운드에서 완료할 때까지 대기</span><span class="sxs-lookup"><span data-stu-id="f2680-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan
PS C:\> $job | Wait-Job
```

<span data-ttu-id="f2680-114">이 명령은 활성 구독에 대 한 정책 준수 평가를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2680-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="f2680-115">검사가 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="f2680-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="f2680-116">변수</span><span class="sxs-lookup"><span data-stu-id="f2680-116">PARAMETERS</span></span>

### <span data-ttu-id="f2680-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2680-117">-AsJob</span></span>
<span data-ttu-id="f2680-118">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2680-118">Run cmdlet in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2680-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2680-119">-DefaultProfile</span></span>
<span data-ttu-id="f2680-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2680-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2680-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2680-121">-PassThru</span></span>
<span data-ttu-id="f2680-122">명령이 성공적으로 완료 되 면 True를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2680-122">Return True if the command completes successfully.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2680-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2680-123">-ResourceGroupName</span></span>
<span data-ttu-id="f2680-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2680-124">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2680-125">-확인</span><span class="sxs-lookup"><span data-stu-id="f2680-125">-Confirm</span></span>
<span data-ttu-id="f2680-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2680-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2680-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2680-127">-WhatIf</span></span>
<span data-ttu-id="f2680-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f2680-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2680-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2680-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2680-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2680-130">CommonParameters</span></span>
<span data-ttu-id="f2680-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2680-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2680-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f2680-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2680-133">입력</span><span class="sxs-lookup"><span data-stu-id="f2680-133">INPUTS</span></span>

### <span data-ttu-id="f2680-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f2680-134">System.String</span></span>

## <span data-ttu-id="f2680-135">출력</span><span class="sxs-lookup"><span data-stu-id="f2680-135">OUTPUTS</span></span>

### <span data-ttu-id="f2680-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f2680-136">System.Boolean</span></span>

## <span data-ttu-id="f2680-137">상속자</span><span class="sxs-lookup"><span data-stu-id="f2680-137">NOTES</span></span>

## <span data-ttu-id="f2680-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2680-138">RELATED LINKS</span></span>
