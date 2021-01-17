---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 556cc10b415b2e37b832f144a01d307a2b69e52d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489211"
---
# <span data-ttu-id="33739-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="33739-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="33739-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33739-102">SYNOPSIS</span></span>
<span data-ttu-id="33739-103">지정된 Azure Data Lake Analytics 계산 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="33739-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="33739-104">구문</span><span class="sxs-lookup"><span data-stu-id="33739-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33739-105">설명</span><span class="sxs-lookup"><span data-stu-id="33739-105">DESCRIPTION</span></span>
<span data-ttu-id="33739-106">**Remove-AzDataLakeAnalyticsComputePolicy는** 지정된 Azure Data Lake Analytics 계산 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="33739-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="33739-107">예제</span><span class="sxs-lookup"><span data-stu-id="33739-107">EXAMPLES</span></span>

### <span data-ttu-id="33739-108">예제 1: 계산 정책 제거</span><span class="sxs-lookup"><span data-stu-id="33739-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="33739-109">이 명령은 계정 'contosoadla'에서 이름이 'myPolicy'인 지정된 계산 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="33739-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="33739-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33739-110">PARAMETERS</span></span>

### <span data-ttu-id="33739-111">-Account</span><span class="sxs-lookup"><span data-stu-id="33739-111">-Account</span></span>
<span data-ttu-id="33739-112">계산 정책을 제거할 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33739-112">Name of the account to remove the compute policy from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33739-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33739-113">-DefaultProfile</span></span>
<span data-ttu-id="33739-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="33739-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33739-115">-Name</span><span class="sxs-lookup"><span data-stu-id="33739-115">-Name</span></span>
<span data-ttu-id="33739-116">제거할 계산 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33739-116">Name of the compute policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33739-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33739-117">-PassThru</span></span>
<span data-ttu-id="33739-118">성공적으로 지우면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="33739-118">Return true upon successful deletion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33739-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33739-119">-ResourceGroupName</span></span>
<span data-ttu-id="33739-120">계정이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33739-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="33739-121">선택 사항이며, 제공되지 않은 경우 검색을 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="33739-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="33739-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33739-122">-Confirm</span></span>
<span data-ttu-id="33739-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="33739-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33739-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33739-124">-WhatIf</span></span>
<span data-ttu-id="33739-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="33739-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33739-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33739-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33739-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33739-127">CommonParameters</span></span>
<span data-ttu-id="33739-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="33739-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33739-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="33739-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33739-130">입력</span><span class="sxs-lookup"><span data-stu-id="33739-130">INPUTS</span></span>

### <span data-ttu-id="33739-131">System.String</span><span class="sxs-lookup"><span data-stu-id="33739-131">System.String</span></span>

## <span data-ttu-id="33739-132">출력</span><span class="sxs-lookup"><span data-stu-id="33739-132">OUTPUTS</span></span>

### <span data-ttu-id="33739-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="33739-133">System.Boolean</span></span>

## <span data-ttu-id="33739-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="33739-134">NOTES</span></span>

## <span data-ttu-id="33739-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33739-135">RELATED LINKS</span></span>
