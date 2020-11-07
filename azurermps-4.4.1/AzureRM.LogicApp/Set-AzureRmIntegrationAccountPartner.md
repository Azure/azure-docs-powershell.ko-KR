---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 13b82cbc7b1f83c441f1211f6ebe7aa1f8c59ea5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703705"
---
# <span data-ttu-id="65e3e-101">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="65e3e-101">Set-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="65e3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="65e3e-103">통합 계정 파트너를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-103">Modifies an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65e3e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65e3e-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65e3e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="65e3e-105">DESCRIPTION</span></span>
<span data-ttu-id="65e3e-106">**Set-AzureRmIntegrationAccountPartner** cmdlet은 통합 계정 파트너를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-106">The **Set-AzureRmIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="65e3e-107">이 cmdlet은 통합 계정 파트너를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="65e3e-108">통합 계정 이름, 리소스 그룹 이름, 파트너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-108">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="65e3e-109">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="65e3e-110">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="65e3e-111">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="65e3e-112">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="65e3e-113">예제의</span><span class="sxs-lookup"><span data-stu-id="65e3e-113">EXAMPLES</span></span>

### <span data-ttu-id="65e3e-114">예제 1: 통합 계정 파트너 수정</span><span class="sxs-lookup"><span data-stu-id="65e3e-114">Example 1: Modify an integration account partner</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="65e3e-115">이 명령은 지정 된 리소스 그룹에서 IntegrationAccountPartner22 이라는 통합 계정 파트너를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="65e3e-116">변수</span><span class="sxs-lookup"><span data-stu-id="65e3e-116">PARAMETERS</span></span>

### <span data-ttu-id="65e3e-117">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="65e3e-117">-BusinessIdentities</span></span>
<span data-ttu-id="65e3e-118">통합 계정 파트너에 대 한 비즈니스 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-118">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="65e3e-119">해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-119">Specify a hash table.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e3e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="65e3e-120">-Force</span></span>
<span data-ttu-id="65e3e-121">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="65e3e-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="65e3e-122">-Metadata</span></span>
<span data-ttu-id="65e3e-123">파트너에 대 한 메타 데이터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-123">Specifies a metadata object for the partner.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e3e-124">-이름</span><span class="sxs-lookup"><span data-stu-id="65e3e-124">-Name</span></span>
<span data-ttu-id="65e3e-125">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-125">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65e3e-126">-(이름)</span><span class="sxs-lookup"><span data-stu-id="65e3e-126">-PartnerName</span></span>
<span data-ttu-id="65e3e-127">통합 계정 파트너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-127">Specifies the name of the integration account partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65e3e-128">-용 유형</span><span class="sxs-lookup"><span data-stu-id="65e3e-128">-PartnerType</span></span>
<span data-ttu-id="65e3e-129">통합 계정의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-129">Specifies the type of the integration account.</span></span>
<span data-ttu-id="65e3e-130">이 매개 변수는 B2B 유형을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-130">This parameter supports the type B2B.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e3e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65e3e-131">-ResourceGroupName</span></span>
<span data-ttu-id="65e3e-132">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-132">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65e3e-133">-확인</span><span class="sxs-lookup"><span data-stu-id="65e3e-133">-Confirm</span></span>
<span data-ttu-id="65e3e-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e3e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65e3e-135">-WhatIf</span></span>
<span data-ttu-id="65e3e-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65e3e-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e3e-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65e3e-138">-DefaultProfile</span></span>
<span data-ttu-id="65e3e-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e3e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65e3e-140">CommonParameters</span></span>
<span data-ttu-id="65e3e-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e3e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65e3e-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65e3e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65e3e-143">입력</span><span class="sxs-lookup"><span data-stu-id="65e3e-143">INPUTS</span></span>

## <span data-ttu-id="65e3e-144">출력</span><span class="sxs-lookup"><span data-stu-id="65e3e-144">OUTPUTS</span></span>

### <span data-ttu-id="65e3e-145">IntegrationAccountPartner를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="65e3e-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="65e3e-146">상속자</span><span class="sxs-lookup"><span data-stu-id="65e3e-146">NOTES</span></span>

## <span data-ttu-id="65e3e-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65e3e-147">RELATED LINKS</span></span>

[<span data-ttu-id="65e3e-148">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="65e3e-148">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="65e3e-149">새로운 AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="65e3e-149">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="65e3e-150">제거-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="65e3e-150">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)


