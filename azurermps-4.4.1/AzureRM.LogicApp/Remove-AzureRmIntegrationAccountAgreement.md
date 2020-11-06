---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 63241b764576e06166e293f17717b26c4dcbe3d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533064"
---
# <span data-ttu-id="abc1b-101">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="abc1b-101">Remove-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="abc1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abc1b-102">SYNOPSIS</span></span>
<span data-ttu-id="abc1b-103">통합 계정 계약을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="abc1b-103">Removes an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abc1b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="abc1b-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abc1b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="abc1b-105">DESCRIPTION</span></span>
<span data-ttu-id="abc1b-106">**AzureRmIntegrationAccountAgreement** Cmdlet는 Azure 리소스 그룹의 통합 계정 계약을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="abc1b-106">The **Remove-AzureRmIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="abc1b-107">통합 계정 이름, 리소스 그룹 이름 및 규약 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="abc1b-107">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="abc1b-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="abc1b-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="abc1b-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="abc1b-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="abc1b-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="abc1b-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="abc1b-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="abc1b-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="abc1b-112">예제의</span><span class="sxs-lookup"><span data-stu-id="abc1b-112">EXAMPLES</span></span>

### <span data-ttu-id="abc1b-113">예제 1: 이름별 통합 계정 계약 제거</span><span class="sxs-lookup"><span data-stu-id="abc1b-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="abc1b-114">이 명령은 IntegrationAccountAgreement06 이라는 통합 계정 계약을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="abc1b-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="abc1b-115">명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abc1b-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="abc1b-116">변수</span><span class="sxs-lookup"><span data-stu-id="abc1b-116">PARAMETERS</span></span>

### <span data-ttu-id="abc1b-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="abc1b-117">-AgreementName</span></span>
<span data-ttu-id="abc1b-118">통합 계정 계약의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="abc1b-118">Specifies the name of the integration account agreement.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abc1b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="abc1b-119">-Force</span></span>
<span data-ttu-id="abc1b-120">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="abc1b-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="abc1b-121">-이름</span><span class="sxs-lookup"><span data-stu-id="abc1b-121">-Name</span></span>
<span data-ttu-id="abc1b-122">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="abc1b-122">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abc1b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abc1b-123">-ResourceGroupName</span></span>
<span data-ttu-id="abc1b-124">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="abc1b-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="abc1b-125">-확인</span><span class="sxs-lookup"><span data-stu-id="abc1b-125">-Confirm</span></span>
<span data-ttu-id="abc1b-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="abc1b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abc1b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abc1b-127">-WhatIf</span></span>
<span data-ttu-id="abc1b-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="abc1b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abc1b-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abc1b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abc1b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc1b-130">-DefaultProfile</span></span>
<span data-ttu-id="abc1b-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="abc1b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abc1b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc1b-132">CommonParameters</span></span>
<span data-ttu-id="abc1b-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="abc1b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc1b-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abc1b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc1b-135">입력</span><span class="sxs-lookup"><span data-stu-id="abc1b-135">INPUTS</span></span>

## <span data-ttu-id="abc1b-136">출력</span><span class="sxs-lookup"><span data-stu-id="abc1b-136">OUTPUTS</span></span>

## <span data-ttu-id="abc1b-137">상속자</span><span class="sxs-lookup"><span data-stu-id="abc1b-137">NOTES</span></span>

## <span data-ttu-id="abc1b-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="abc1b-138">RELATED LINKS</span></span>

[<span data-ttu-id="abc1b-139">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="abc1b-139">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="abc1b-140">새로운 AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="abc1b-140">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="abc1b-141">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="abc1b-141">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


