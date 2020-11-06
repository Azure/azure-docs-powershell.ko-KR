---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
ms.openlocfilehash: d2948378f9312687e2dbbe09bd7c583cbe085778
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529795"
---
# <span data-ttu-id="e749f-101">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="e749f-101">Set-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="e749f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e749f-102">SYNOPSIS</span></span>
<span data-ttu-id="e749f-103">통합 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e749f-103">Modifies an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e749f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e749f-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e749f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e749f-105">DESCRIPTION</span></span>
<span data-ttu-id="e749f-106">**Set-AzureRmIntegrationAccount** cmdlet은 통합 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e749f-106">The **Set-AzureRmIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="e749f-107">이 cmdlet은 통합 계정을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e749f-107">This cmdlet returns an object that represents the integration account.</span></span>

<span data-ttu-id="e749f-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e749f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e749f-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="e749f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e749f-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e749f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e749f-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e749f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e749f-112">예제의</span><span class="sxs-lookup"><span data-stu-id="e749f-112">EXAMPLES</span></span>

### <span data-ttu-id="e749f-113">예제 1: 통합 계정 수정</span><span class="sxs-lookup"><span data-stu-id="e749f-113">Example 1: Modify an integration account</span></span>
```
PS C:\>Set-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Sku "Free"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="e749f-114">이 명령은 지정 된 리소스 그룹의 IntegrationAccount31 이라는 통합 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e749f-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="e749f-115">변수</span><span class="sxs-lookup"><span data-stu-id="e749f-115">PARAMETERS</span></span>

### <span data-ttu-id="e749f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e749f-116">-DefaultProfile</span></span>
<span data-ttu-id="e749f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e749f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e749f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e749f-118">-Force</span></span>
<span data-ttu-id="e749f-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e749f-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e749f-120">-위치</span><span class="sxs-lookup"><span data-stu-id="e749f-120">-Location</span></span>
<span data-ttu-id="e749f-121">통합 계정의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e749f-121">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="e749f-122">-이름</span><span class="sxs-lookup"><span data-stu-id="e749f-122">-Name</span></span>
<span data-ttu-id="e749f-123">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e749f-123">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e749f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e749f-124">-ResourceGroupName</span></span>
<span data-ttu-id="e749f-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e749f-125">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e749f-126">-Sku</span><span class="sxs-lookup"><span data-stu-id="e749f-126">-Sku</span></span>
<span data-ttu-id="e749f-127">통합 계정에 대 한 SKU 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e749f-127">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="e749f-128">-확인</span><span class="sxs-lookup"><span data-stu-id="e749f-128">-Confirm</span></span>
<span data-ttu-id="e749f-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e749f-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e749f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e749f-130">-WhatIf</span></span>
<span data-ttu-id="e749f-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e749f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e749f-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e749f-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e749f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e749f-133">CommonParameters</span></span>
<span data-ttu-id="e749f-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e749f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e749f-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e749f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e749f-136">입력</span><span class="sxs-lookup"><span data-stu-id="e749f-136">INPUTS</span></span>

### <span data-ttu-id="e749f-137">않아야</span><span class="sxs-lookup"><span data-stu-id="e749f-137">None</span></span>
<span data-ttu-id="e749f-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e749f-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e749f-139">출력</span><span class="sxs-lookup"><span data-stu-id="e749f-139">OUTPUTS</span></span>

### <span data-ttu-id="e749f-140">IntegrationAccount를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="e749f-140">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="e749f-141">상속자</span><span class="sxs-lookup"><span data-stu-id="e749f-141">NOTES</span></span>

## <span data-ttu-id="e749f-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e749f-142">RELATED LINKS</span></span>

[<span data-ttu-id="e749f-143">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="e749f-143">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="e749f-144">새로운 AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="e749f-144">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="e749f-145">제거-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="e749f-145">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)


