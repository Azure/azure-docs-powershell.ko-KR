---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: deafb0cb68ab58997df83bc0280b50a4cc4a0de0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696903"
---
# <span data-ttu-id="4f269-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="4f269-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="4f269-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f269-102">SYNOPSIS</span></span>
<span data-ttu-id="4f269-103">지정 된 Azure Data Lake Analytics 계산 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f269-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="4f269-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4f269-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f269-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4f269-105">DESCRIPTION</span></span>
<span data-ttu-id="4f269-106">**AzDataLakeAnalyticsComputePolicy 제거** 는 지정 된 Azure Data Lake 분석 계산 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f269-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="4f269-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4f269-107">EXAMPLES</span></span>

### <span data-ttu-id="4f269-108">예제 1: 계산 정책 제거</span><span class="sxs-lookup"><span data-stu-id="4f269-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="4f269-109">이 명령은 ' contosoadla ' 계정에서 이름이 ' myPolicy ' 인 지정 된 계산 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f269-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="4f269-110">변수</span><span class="sxs-lookup"><span data-stu-id="4f269-110">PARAMETERS</span></span>

### <span data-ttu-id="4f269-111">-계정</span><span class="sxs-lookup"><span data-stu-id="4f269-111">-Account</span></span>
<span data-ttu-id="4f269-112">계산 정책을 제거할 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f269-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="4f269-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f269-113">-DefaultProfile</span></span>
<span data-ttu-id="4f269-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4f269-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f269-115">-이름</span><span class="sxs-lookup"><span data-stu-id="4f269-115">-Name</span></span>
<span data-ttu-id="4f269-116">제거할 계산 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f269-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="4f269-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f269-117">-PassThru</span></span>
<span data-ttu-id="4f269-118">삭제에 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f269-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="4f269-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f269-119">-ResourceGroupName</span></span>
<span data-ttu-id="4f269-120">계정이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f269-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="4f269-121">선택 사항이 며 제공 되지 않은 경우 검색을 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f269-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="4f269-122">-확인</span><span class="sxs-lookup"><span data-stu-id="4f269-122">-Confirm</span></span>
<span data-ttu-id="4f269-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f269-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f269-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f269-124">-WhatIf</span></span>
<span data-ttu-id="4f269-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4f269-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f269-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f269-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f269-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f269-127">CommonParameters</span></span>
<span data-ttu-id="4f269-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f269-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f269-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f269-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f269-130">입력</span><span class="sxs-lookup"><span data-stu-id="4f269-130">INPUTS</span></span>

### <span data-ttu-id="4f269-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4f269-131">System.String</span></span>

## <span data-ttu-id="4f269-132">출력</span><span class="sxs-lookup"><span data-stu-id="4f269-132">OUTPUTS</span></span>

### <span data-ttu-id="4f269-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="4f269-133">System.Boolean</span></span>

## <span data-ttu-id="4f269-134">상속자</span><span class="sxs-lookup"><span data-stu-id="4f269-134">NOTES</span></span>

## <span data-ttu-id="4f269-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f269-135">RELATED LINKS</span></span>
