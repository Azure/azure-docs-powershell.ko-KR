---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: db51cfdf499fcf3d6c81f47d977978a6ff4bf8cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989072"
---
# <span data-ttu-id="ca0ae-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="ca0ae-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="ca0ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca0ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ca0ae-103">구독 또는 리소스 그룹의 모든 리소스에 대한 정책 준수 평가를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="ca0ae-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="ca0ae-104">구문</span><span class="sxs-lookup"><span data-stu-id="ca0ae-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca0ae-105">설명</span><span class="sxs-lookup"><span data-stu-id="ca0ae-105">DESCRIPTION</span></span>
<span data-ttu-id="ca0ae-106">**Start-AzPolicyComplianceScan** cmdlet은 구독 또는 리소스 그룹에 대한 정책 준수 평가를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="ca0ae-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="ca0ae-107">해당 범위 내의 모든 리소스는 할당된 모든 정책에 대해 규정 준수 상태를 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="ca0ae-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="ca0ae-108">예제</span><span class="sxs-lookup"><span data-stu-id="ca0ae-108">EXAMPLES</span></span>

### <span data-ttu-id="ca0ae-109">예제 1: 구독 범위에서 규정 준수 검사 시작</span><span class="sxs-lookup"><span data-stu-id="ca0ae-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="ca0ae-110">이 명령은 활성 구독에 대한 정책 준수 평가를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="ca0ae-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="ca0ae-111">예제 2: 리소스 그룹 범위에서 규정 준수 검사 시작</span><span class="sxs-lookup"><span data-stu-id="ca0ae-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="ca0ae-112">이 명령은 활성 구독의 "myRG" 리소스 그룹에 대한 정책 준수 평가를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="ca0ae-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="ca0ae-113">예제 3: 규정 준수 검사 시작 및 백그라운드에서 완료될 때까지 기다림</span><span class="sxs-lookup"><span data-stu-id="ca0ae-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

<span data-ttu-id="ca0ae-114">이 명령은 활성 구독에 대한 정책 준수 평가를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="ca0ae-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="ca0ae-115">검사가 완료될 때까지 기다릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca0ae-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="ca0ae-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ca0ae-116">PARAMETERS</span></span>

### <span data-ttu-id="ca0ae-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca0ae-117">-AsJob</span></span>
<span data-ttu-id="ca0ae-118">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ca0ae-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ca0ae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca0ae-119">-DefaultProfile</span></span>
<span data-ttu-id="ca0ae-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca0ae-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca0ae-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca0ae-121">-PassThru</span></span>
<span data-ttu-id="ca0ae-122">명령이 성공적으로 완료되면 True를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ca0ae-122">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="ca0ae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca0ae-123">-ResourceGroupName</span></span>
<span data-ttu-id="ca0ae-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca0ae-124">Resource group name.</span></span>

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

### <span data-ttu-id="ca0ae-125">-확인</span><span class="sxs-lookup"><span data-stu-id="ca0ae-125">-Confirm</span></span>
<span data-ttu-id="ca0ae-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca0ae-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca0ae-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca0ae-127">-WhatIf</span></span>
<span data-ttu-id="ca0ae-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ca0ae-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca0ae-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca0ae-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca0ae-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca0ae-130">CommonParameters</span></span>
<span data-ttu-id="ca0ae-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ca0ae-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca0ae-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca0ae-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca0ae-133">입력</span><span class="sxs-lookup"><span data-stu-id="ca0ae-133">INPUTS</span></span>

### <span data-ttu-id="ca0ae-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ca0ae-134">System.String</span></span>

## <span data-ttu-id="ca0ae-135">출력</span><span class="sxs-lookup"><span data-stu-id="ca0ae-135">OUTPUTS</span></span>

### <span data-ttu-id="ca0ae-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ca0ae-136">System.Boolean</span></span>

## <span data-ttu-id="ca0ae-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ca0ae-137">NOTES</span></span>

## <span data-ttu-id="ca0ae-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca0ae-138">RELATED LINKS</span></span>
