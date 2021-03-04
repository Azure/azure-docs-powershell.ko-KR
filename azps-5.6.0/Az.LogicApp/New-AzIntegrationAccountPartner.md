---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
ms.openlocfilehash: 7b07a07dc99efa7f0f3fdb150c902b86b374181e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958683"
---
# <span data-ttu-id="c02ac-101">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="c02ac-101">New-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="c02ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c02ac-102">SYNOPSIS</span></span>
<span data-ttu-id="c02ac-103">통합 계정 파트너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-103">Creates an integration account partner.</span></span>

## <span data-ttu-id="c02ac-104">구문</span><span class="sxs-lookup"><span data-stu-id="c02ac-104">SYNTAX</span></span>

```
New-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c02ac-105">설명</span><span class="sxs-lookup"><span data-stu-id="c02ac-105">DESCRIPTION</span></span>
<span data-ttu-id="c02ac-106">**New-AzIntegrationAccountPartner** cmdlet은 통합 계정 파트너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-106">The **New-AzIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="c02ac-107">이 cmdlet은 통합 계정 파트너를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="c02ac-108">통합 계정 이름, 리소스 그룹 이름, 파트너 이름 및 파트너 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>
<span data-ttu-id="c02ac-109">명령줄에서 지정한 템플릿 매개 변수 파일 값은 템플릿 매개 변수 개체의 템플릿 매개 변수 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="c02ac-110">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c02ac-111">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c02ac-112">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 뒤 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c02ac-113">필요한 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c02ac-114">예제</span><span class="sxs-lookup"><span data-stu-id="c02ac-114">EXAMPLES</span></span>

### <span data-ttu-id="c02ac-115">예제 1: 통합 계정 파트너 만들기</span><span class="sxs-lookup"><span data-stu-id="c02ac-115">Example 1: Create an integration account partner</span></span>
```
PS C:\>New-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata           :
```

<span data-ttu-id="c02ac-116">이 명령은 지정된 리소스 그룹에 IntegrationAccountPartner22라는 통합 계정 파트너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="c02ac-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c02ac-117">PARAMETERS</span></span>

### <span data-ttu-id="c02ac-118">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="c02ac-118">-BusinessIdentities</span></span>
<span data-ttu-id="c02ac-119">통합 계정 파트너에 대한 비즈니스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="c02ac-120">해시 테이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-120">Specify a hash table.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c02ac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c02ac-121">-DefaultProfile</span></span>
<span data-ttu-id="c02ac-122">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c02ac-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c02ac-123">-메타데이터</span><span class="sxs-lookup"><span data-stu-id="c02ac-123">-Metadata</span></span>
<span data-ttu-id="c02ac-124">파트너에 대한 메타데이터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-124">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="c02ac-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c02ac-125">-Name</span></span>
<span data-ttu-id="c02ac-126">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-126">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="c02ac-127">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="c02ac-127">-PartnerName</span></span>
<span data-ttu-id="c02ac-128">통합 계정 파트너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-128">Specifies a name for the integration account partner.</span></span>

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

### <span data-ttu-id="c02ac-129">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="c02ac-129">-PartnerType</span></span>
<span data-ttu-id="c02ac-130">통합 계정의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-130">Specifies the type of the integration account.</span></span>
<span data-ttu-id="c02ac-131">이 매개 변수는 B2B 형식을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-131">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="c02ac-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c02ac-132">-ResourceGroupName</span></span>
<span data-ttu-id="c02ac-133">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-133">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c02ac-134">-확인</span><span class="sxs-lookup"><span data-stu-id="c02ac-134">-Confirm</span></span>
<span data-ttu-id="c02ac-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c02ac-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c02ac-136">-WhatIf</span></span>
<span data-ttu-id="c02ac-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c02ac-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c02ac-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c02ac-139">CommonParameters</span></span>
<span data-ttu-id="c02ac-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ac-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c02ac-141">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c02ac-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c02ac-142">입력</span><span class="sxs-lookup"><span data-stu-id="c02ac-142">INPUTS</span></span>

### <span data-ttu-id="c02ac-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c02ac-143">System.String</span></span>

## <span data-ttu-id="c02ac-144">출력</span><span class="sxs-lookup"><span data-stu-id="c02ac-144">OUTPUTS</span></span>

### <span data-ttu-id="c02ac-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="c02ac-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="c02ac-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c02ac-146">NOTES</span></span>

## <span data-ttu-id="c02ac-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c02ac-147">RELATED LINKS</span></span>

[<span data-ttu-id="c02ac-148">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="c02ac-148">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="c02ac-149">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="c02ac-149">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="c02ac-150">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="c02ac-150">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


