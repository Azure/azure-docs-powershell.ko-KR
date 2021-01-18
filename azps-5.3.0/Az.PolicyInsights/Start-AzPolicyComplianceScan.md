---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: 61022603ad34c345274328d47767e90580e54d6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496307"
---
# <span data-ttu-id="19bd3-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="19bd3-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="19bd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="19bd3-103">구독 또는 리소스 그룹의 모든 리소스에 대한 정책 준수 평가를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="19bd3-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="19bd3-104">구문</span><span class="sxs-lookup"><span data-stu-id="19bd3-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19bd3-105">설명</span><span class="sxs-lookup"><span data-stu-id="19bd3-105">DESCRIPTION</span></span>
<span data-ttu-id="19bd3-106">**Start-AzPolicyComplianceScan** cmdlet은 구독 또는 리소스 그룹에 대한 정책 준수 평가를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="19bd3-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="19bd3-107">해당 범위 내의 모든 리소스는 할당된 모든 정책에 대해 규정 준수 상태를 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="19bd3-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="19bd3-108">예제</span><span class="sxs-lookup"><span data-stu-id="19bd3-108">EXAMPLES</span></span>

### <span data-ttu-id="19bd3-109">예제 1: 구독 범위에서 규정 준수 검사 시작</span><span class="sxs-lookup"><span data-stu-id="19bd3-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="19bd3-110">이 명령은 활성 구독에 대한 정책 준수 평가를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="19bd3-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="19bd3-111">예제 2: 리소스 그룹 범위에서 규정 준수 검사 시작</span><span class="sxs-lookup"><span data-stu-id="19bd3-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="19bd3-112">이 명령은 활성 구독의 "myRG" 리소스 그룹에 대한 정책 준수 평가를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="19bd3-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="19bd3-113">예제 3: 규정 준수 검색을 시작하고 백그라운드에서 완료될 때까지 기다림</span><span class="sxs-lookup"><span data-stu-id="19bd3-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

<span data-ttu-id="19bd3-114">이 명령은 활성 구독에 대한 정책 준수 평가를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="19bd3-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="19bd3-115">검색이 완료될 때까지 기다릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19bd3-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="19bd3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19bd3-116">PARAMETERS</span></span>

### <span data-ttu-id="19bd3-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19bd3-117">-AsJob</span></span>
<span data-ttu-id="19bd3-118">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="19bd3-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="19bd3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19bd3-119">-DefaultProfile</span></span>
<span data-ttu-id="19bd3-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19bd3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19bd3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19bd3-121">-PassThru</span></span>
<span data-ttu-id="19bd3-122">명령이 성공적으로 완료되면 True를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="19bd3-122">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="19bd3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19bd3-123">-ResourceGroupName</span></span>
<span data-ttu-id="19bd3-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19bd3-124">Resource group name.</span></span>

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

### <span data-ttu-id="19bd3-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19bd3-125">-Confirm</span></span>
<span data-ttu-id="19bd3-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="19bd3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19bd3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19bd3-127">-WhatIf</span></span>
<span data-ttu-id="19bd3-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="19bd3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19bd3-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19bd3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19bd3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19bd3-130">CommonParameters</span></span>
<span data-ttu-id="19bd3-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="19bd3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19bd3-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="19bd3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19bd3-133">입력</span><span class="sxs-lookup"><span data-stu-id="19bd3-133">INPUTS</span></span>

### <span data-ttu-id="19bd3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="19bd3-134">System.String</span></span>

## <span data-ttu-id="19bd3-135">출력</span><span class="sxs-lookup"><span data-stu-id="19bd3-135">OUTPUTS</span></span>

### <span data-ttu-id="19bd3-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="19bd3-136">System.Boolean</span></span>

## <span data-ttu-id="19bd3-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="19bd3-137">NOTES</span></span>

## <span data-ttu-id="19bd3-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19bd3-138">RELATED LINKS</span></span>
