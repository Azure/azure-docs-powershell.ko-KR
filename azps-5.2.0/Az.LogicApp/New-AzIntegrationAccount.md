---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
ms.openlocfilehash: a3a3fc16b253235da82626ab6d827d074f05860d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333950"
---
# <span data-ttu-id="9fb46-101">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="9fb46-101">New-AzIntegrationAccount</span></span>

## <span data-ttu-id="9fb46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fb46-102">SYNOPSIS</span></span>
<span data-ttu-id="9fb46-103">통합 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9fb46-103">Creates an integration account.</span></span>

## <span data-ttu-id="9fb46-104">구문</span><span class="sxs-lookup"><span data-stu-id="9fb46-104">SYNTAX</span></span>

```
New-AzIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fb46-105">설명</span><span class="sxs-lookup"><span data-stu-id="9fb46-105">DESCRIPTION</span></span>
<span data-ttu-id="9fb46-106">**New-AzIntegrationAccount** cmdlet은 통합 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9fb46-106">The **New-AzIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="9fb46-107">이 cmdlet은 통합 계정을 나타내는 개체를 반환합니다. 이름, 위치, 리소스 그룹 이름 및 SKU 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb46-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>
<span data-ttu-id="9fb46-108">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb46-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="9fb46-109">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb46-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9fb46-110">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb46-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9fb46-111">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb46-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9fb46-112">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="9fb46-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9fb46-113">예제</span><span class="sxs-lookup"><span data-stu-id="9fb46-113">EXAMPLES</span></span>

### <span data-ttu-id="9fb46-114">예제 1: 통합 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="9fb46-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="9fb46-115">이 명령은 지정된 리소스 그룹에 IntegrationAccount31이라는 통합 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9fb46-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="9fb46-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fb46-116">PARAMETERS</span></span>

### <span data-ttu-id="9fb46-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fb46-117">-DefaultProfile</span></span>
<span data-ttu-id="9fb46-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9fb46-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fb46-119">-Location</span><span class="sxs-lookup"><span data-stu-id="9fb46-119">-Location</span></span>
<span data-ttu-id="9fb46-120">통합 계정의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb46-120">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="9fb46-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9fb46-121">-Name</span></span>
<span data-ttu-id="9fb46-122">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb46-122">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="9fb46-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fb46-123">-ResourceGroupName</span></span>
<span data-ttu-id="9fb46-124">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb46-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9fb46-125">-Sku</span><span class="sxs-lookup"><span data-stu-id="9fb46-125">-Sku</span></span>
<span data-ttu-id="9fb46-126">통합 계정에 대한 SKU 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb46-126">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb46-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fb46-127">-Confirm</span></span>
<span data-ttu-id="9fb46-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9fb46-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fb46-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fb46-129">-WhatIf</span></span>
<span data-ttu-id="9fb46-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9fb46-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fb46-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9fb46-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fb46-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fb46-132">CommonParameters</span></span>
<span data-ttu-id="9fb46-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb46-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fb46-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9fb46-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fb46-135">입력</span><span class="sxs-lookup"><span data-stu-id="9fb46-135">INPUTS</span></span>

### <span data-ttu-id="9fb46-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9fb46-136">System.String</span></span>

## <span data-ttu-id="9fb46-137">출력</span><span class="sxs-lookup"><span data-stu-id="9fb46-137">OUTPUTS</span></span>

### <span data-ttu-id="9fb46-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="9fb46-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="9fb46-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9fb46-139">NOTES</span></span>

## <span data-ttu-id="9fb46-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9fb46-140">RELATED LINKS</span></span>

[<span data-ttu-id="9fb46-141">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="9fb46-141">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="9fb46-142">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="9fb46-142">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="9fb46-143">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="9fb46-143">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


