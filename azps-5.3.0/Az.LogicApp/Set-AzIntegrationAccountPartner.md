---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
ms.openlocfilehash: edd50a72ed0614cf7c71dfbde9f487e8fe632d85
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490155"
---
# <span data-ttu-id="0c74c-101">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="0c74c-101">Set-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="0c74c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c74c-102">SYNOPSIS</span></span>
<span data-ttu-id="0c74c-103">통합 계정 파트너를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-103">Modifies an integration account partner.</span></span>

## <span data-ttu-id="0c74c-104">구문</span><span class="sxs-lookup"><span data-stu-id="0c74c-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c74c-105">설명</span><span class="sxs-lookup"><span data-stu-id="0c74c-105">DESCRIPTION</span></span>
<span data-ttu-id="0c74c-106">**Set-AzIntegrationAccountPartner** cmdlet은 통합 계정 파트너를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-106">The **Set-AzIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="0c74c-107">이 cmdlet은 통합 계정 파트너를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="0c74c-108">통합 계정 이름, 리소스 그룹 이름 및 파트너 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-108">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="0c74c-109">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0c74c-110">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0c74c-111">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0c74c-112">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0c74c-113">예제</span><span class="sxs-lookup"><span data-stu-id="0c74c-113">EXAMPLES</span></span>

### <span data-ttu-id="0c74c-114">예제 1: 통합 계정 파트너 수정</span><span class="sxs-lookup"><span data-stu-id="0c74c-114">Example 1: Modify an integration account partner</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="0c74c-115">이 명령은 지정된 리소스 그룹에서 IntegrationAccountPartner22라는 통합 계정 파트너를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

### <span data-ttu-id="0c74c-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="0c74c-116">Example 2</span></span>

<span data-ttu-id="0c74c-117">통합 계정 파트너를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-117">Modifies an integration account partner.</span></span> <span data-ttu-id="0c74c-118">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="0c74c-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountPartner -BusinessIdentities <Object> -Metadata <Object> -Name 'IntegrationAccount31' -PartnerName 'IntegrationAccountPartner22' -PartnerType B2B -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="0c74c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c74c-119">PARAMETERS</span></span>

### <span data-ttu-id="0c74c-120">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="0c74c-120">-BusinessIdentities</span></span>
<span data-ttu-id="0c74c-121">통합 계정 파트너의 비즈니스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-121">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="0c74c-122">해시 테이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-122">Specify a hash table.</span></span>

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

### <span data-ttu-id="0c74c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c74c-123">-DefaultProfile</span></span>
<span data-ttu-id="0c74c-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0c74c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c74c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="0c74c-125">-Force</span></span>
<span data-ttu-id="0c74c-126">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0c74c-127">-Metadata</span><span class="sxs-lookup"><span data-stu-id="0c74c-127">-Metadata</span></span>
<span data-ttu-id="0c74c-128">파트너에 대한 메타데이터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-128">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="0c74c-129">-Name</span><span class="sxs-lookup"><span data-stu-id="0c74c-129">-Name</span></span>
<span data-ttu-id="0c74c-130">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-130">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="0c74c-131">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="0c74c-131">-PartnerName</span></span>
<span data-ttu-id="0c74c-132">통합 계정 파트너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-132">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="0c74c-133">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="0c74c-133">-PartnerType</span></span>
<span data-ttu-id="0c74c-134">통합 계정의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-134">Specifies the type of the integration account.</span></span>
<span data-ttu-id="0c74c-135">이 매개 변수는 B2B 형식을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-135">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="0c74c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c74c-136">-ResourceGroupName</span></span>
<span data-ttu-id="0c74c-137">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-137">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0c74c-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c74c-138">-Confirm</span></span>
<span data-ttu-id="0c74c-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c74c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c74c-140">-WhatIf</span></span>
<span data-ttu-id="0c74c-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0c74c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c74c-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c74c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c74c-143">CommonParameters</span></span>
<span data-ttu-id="0c74c-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0c74c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c74c-145">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0c74c-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c74c-146">입력</span><span class="sxs-lookup"><span data-stu-id="0c74c-146">INPUTS</span></span>

### <span data-ttu-id="0c74c-147">System.String</span><span class="sxs-lookup"><span data-stu-id="0c74c-147">System.String</span></span>

## <span data-ttu-id="0c74c-148">출력</span><span class="sxs-lookup"><span data-stu-id="0c74c-148">OUTPUTS</span></span>

### <span data-ttu-id="0c74c-149">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="0c74c-149">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="0c74c-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0c74c-150">NOTES</span></span>

## <span data-ttu-id="0c74c-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c74c-151">RELATED LINKS</span></span>

[<span data-ttu-id="0c74c-152">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="0c74c-152">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="0c74c-153">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="0c74c-153">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="0c74c-154">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="0c74c-154">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)


