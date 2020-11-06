---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5604430c795f7a318e18b89928c3a75d063a316a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529868"
---
# <span data-ttu-id="adbc1-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="adbc1-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="adbc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adbc1-102">SYNOPSIS</span></span>
<span data-ttu-id="adbc1-103">지정 된 Azure Data Lake Analytics 계산 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="adbc1-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adbc1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="adbc1-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adbc1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="adbc1-105">DESCRIPTION</span></span>
<span data-ttu-id="adbc1-106">**AzureRmDataLakeAnalyticsComputePolicy 제거** 는 지정 된 Azure Data Lake 분석 계산 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="adbc1-106">The **Remove-AzureRmDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="adbc1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="adbc1-107">EXAMPLES</span></span>

### <span data-ttu-id="adbc1-108">예제 1: 계산 정책 제거</span><span class="sxs-lookup"><span data-stu-id="adbc1-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="adbc1-109">이 명령은 ' contosoadla ' 계정에서 이름이 ' myPolicy ' 인 지정 된 계산 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="adbc1-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="adbc1-110">변수</span><span class="sxs-lookup"><span data-stu-id="adbc1-110">PARAMETERS</span></span>

### <span data-ttu-id="adbc1-111">-계정</span><span class="sxs-lookup"><span data-stu-id="adbc1-111">-Account</span></span>
<span data-ttu-id="adbc1-112">계산 정책을 제거할 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="adbc1-112">Name of the account to remove the compute policy from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adbc1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adbc1-113">-DefaultProfile</span></span>
<span data-ttu-id="adbc1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="adbc1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbc1-115">-이름</span><span class="sxs-lookup"><span data-stu-id="adbc1-115">-Name</span></span>
<span data-ttu-id="adbc1-116">제거할 계산 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="adbc1-116">Name of the compute policy to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adbc1-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="adbc1-117">-PassThru</span></span>
<span data-ttu-id="adbc1-118">삭제에 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="adbc1-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="adbc1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adbc1-119">-ResourceGroupName</span></span>
<span data-ttu-id="adbc1-120">계정이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="adbc1-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="adbc1-121">선택 사항이 며 제공 되지 않은 경우 검색을 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="adbc1-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="adbc1-122">-확인</span><span class="sxs-lookup"><span data-stu-id="adbc1-122">-Confirm</span></span>
<span data-ttu-id="adbc1-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="adbc1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adbc1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adbc1-124">-WhatIf</span></span>
<span data-ttu-id="adbc1-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="adbc1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adbc1-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="adbc1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adbc1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adbc1-127">CommonParameters</span></span>
<span data-ttu-id="adbc1-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="adbc1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adbc1-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adbc1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adbc1-130">입력</span><span class="sxs-lookup"><span data-stu-id="adbc1-130">INPUTS</span></span>

### <span data-ttu-id="adbc1-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="adbc1-131">System.String</span></span>

## <span data-ttu-id="adbc1-132">출력</span><span class="sxs-lookup"><span data-stu-id="adbc1-132">OUTPUTS</span></span>

### <span data-ttu-id="adbc1-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="adbc1-133">System.Boolean</span></span>

## <span data-ttu-id="adbc1-134">상속자</span><span class="sxs-lookup"><span data-stu-id="adbc1-134">NOTES</span></span>

## <span data-ttu-id="adbc1-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="adbc1-135">RELATED LINKS</span></span>

