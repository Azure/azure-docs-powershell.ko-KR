---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 470a400721d911e09c7bed4e51eb6cef39a1dafa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531706"
---
# <span data-ttu-id="67c10-101">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="67c10-101">New-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="67c10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67c10-102">SYNOPSIS</span></span>
<span data-ttu-id="67c10-103">통합 계정 파트너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-103">Creates an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67c10-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67c10-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67c10-105">설명은</span><span class="sxs-lookup"><span data-stu-id="67c10-105">DESCRIPTION</span></span>
<span data-ttu-id="67c10-106">**새 AzureRmIntegrationAccountPartner** cmdlet은 통합 계정 파트너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-106">The **New-AzureRmIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="67c10-107">이 cmdlet은 통합 계정 파트너를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="67c10-108">통합 계정 이름, 리소스 그룹 이름, 파트너 이름, 파트너 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>

<span data-ttu-id="67c10-109">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="67c10-110">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="67c10-111">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="67c10-112">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="67c10-113">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="67c10-114">예제의</span><span class="sxs-lookup"><span data-stu-id="67c10-114">EXAMPLES</span></span>

### <span data-ttu-id="67c10-115">예제 1: 통합 계정 파트너 만들기</span><span class="sxs-lookup"><span data-stu-id="67c10-115">Example 1: Create an integration account partner</span></span>
```
PS C:\>New-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata           :
```

<span data-ttu-id="67c10-116">이 명령은 지정 된 리소스 그룹에 IntegrationAccountPartner22 이라는 통합 계정 파트너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="67c10-117">변수</span><span class="sxs-lookup"><span data-stu-id="67c10-117">PARAMETERS</span></span>

### <span data-ttu-id="67c10-118">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="67c10-118">-BusinessIdentities</span></span>
<span data-ttu-id="67c10-119">통합 계정 파트너에 대 한 비즈니스 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="67c10-120">해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-120">Specify a hash table.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67c10-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67c10-121">-DefaultProfile</span></span>
<span data-ttu-id="67c10-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="67c10-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67c10-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="67c10-123">-Metadata</span></span>
<span data-ttu-id="67c10-124">파트너에 대 한 메타 데이터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-124">Specifies a metadata object for the partner.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67c10-125">-이름</span><span class="sxs-lookup"><span data-stu-id="67c10-125">-Name</span></span>
<span data-ttu-id="67c10-126">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-126">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="67c10-127">-(이름)</span><span class="sxs-lookup"><span data-stu-id="67c10-127">-PartnerName</span></span>
<span data-ttu-id="67c10-128">통합 계정 파트너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-128">Specifies a name for the integration account partner.</span></span>

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

### <span data-ttu-id="67c10-129">-용 유형</span><span class="sxs-lookup"><span data-stu-id="67c10-129">-PartnerType</span></span>
<span data-ttu-id="67c10-130">통합 계정의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-130">Specifies the type of the integration account.</span></span>
<span data-ttu-id="67c10-131">이 매개 변수는 B2B 유형을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-131">This parameter supports the type B2B.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67c10-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67c10-132">-ResourceGroupName</span></span>
<span data-ttu-id="67c10-133">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-133">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="67c10-134">-확인</span><span class="sxs-lookup"><span data-stu-id="67c10-134">-Confirm</span></span>
<span data-ttu-id="67c10-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67c10-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67c10-136">-WhatIf</span></span>
<span data-ttu-id="67c10-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67c10-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67c10-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67c10-139">CommonParameters</span></span>
<span data-ttu-id="67c10-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67c10-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67c10-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67c10-142">입력</span><span class="sxs-lookup"><span data-stu-id="67c10-142">INPUTS</span></span>

### <span data-ttu-id="67c10-143">않아야</span><span class="sxs-lookup"><span data-stu-id="67c10-143">None</span></span>
<span data-ttu-id="67c10-144">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67c10-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="67c10-145">출력</span><span class="sxs-lookup"><span data-stu-id="67c10-145">OUTPUTS</span></span>

### <span data-ttu-id="67c10-146">IntegrationAccountPartner를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="67c10-146">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="67c10-147">상속자</span><span class="sxs-lookup"><span data-stu-id="67c10-147">NOTES</span></span>

## <span data-ttu-id="67c10-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67c10-148">RELATED LINKS</span></span>

[<span data-ttu-id="67c10-149">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="67c10-149">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="67c10-150">제거-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="67c10-150">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="67c10-151">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="67c10-151">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


