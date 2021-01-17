---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 78bf9f5e61a66aee6c34dbeb7002d4b2e88e3b68
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327256"
---
# <span data-ttu-id="71e3d-101">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="71e3d-101">Remove-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="71e3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71e3d-102">SYNOPSIS</span></span>
<span data-ttu-id="71e3d-103">리소스 그룹에서 통합 계정 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="71e3d-103">Removes an integration account certificate from a resource group.</span></span>

## <span data-ttu-id="71e3d-104">구문</span><span class="sxs-lookup"><span data-stu-id="71e3d-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71e3d-105">설명</span><span class="sxs-lookup"><span data-stu-id="71e3d-105">DESCRIPTION</span></span>
<span data-ttu-id="71e3d-106">**Remove-AzIntegrationAccountCertificate** cmdlet은 리소스 그룹에서 통합 계정 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="71e3d-106">The **Remove-AzIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="71e3d-107">통합 계정 이름, 리소스 그룹 이름 및 인증서 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71e3d-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="71e3d-108">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="71e3d-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="71e3d-109">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="71e3d-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="71e3d-110">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="71e3d-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="71e3d-111">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="71e3d-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="71e3d-112">예제</span><span class="sxs-lookup"><span data-stu-id="71e3d-112">EXAMPLES</span></span>

### <span data-ttu-id="71e3d-113">예제 1: 통합 계정 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="71e3d-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="71e3d-114">이 명령은 IntegrationAccount31이라는 통합 계정 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="71e3d-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="71e3d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71e3d-115">PARAMETERS</span></span>

### <span data-ttu-id="71e3d-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="71e3d-116">-CertificateName</span></span>
<span data-ttu-id="71e3d-117">통합 계정 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71e3d-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="71e3d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e3d-118">-DefaultProfile</span></span>
<span data-ttu-id="71e3d-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="71e3d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71e3d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="71e3d-120">-Force</span></span>
<span data-ttu-id="71e3d-121">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="71e3d-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="71e3d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="71e3d-122">-Name</span></span>
<span data-ttu-id="71e3d-123">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71e3d-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="71e3d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71e3d-124">-ResourceGroupName</span></span>
<span data-ttu-id="71e3d-125">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71e3d-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="71e3d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71e3d-126">-Confirm</span></span>
<span data-ttu-id="71e3d-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="71e3d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71e3d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71e3d-128">-WhatIf</span></span>
<span data-ttu-id="71e3d-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="71e3d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71e3d-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71e3d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71e3d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e3d-131">CommonParameters</span></span>
<span data-ttu-id="71e3d-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="71e3d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e3d-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="71e3d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e3d-134">입력</span><span class="sxs-lookup"><span data-stu-id="71e3d-134">INPUTS</span></span>

### <span data-ttu-id="71e3d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="71e3d-135">System.String</span></span>

## <span data-ttu-id="71e3d-136">출력</span><span class="sxs-lookup"><span data-stu-id="71e3d-136">OUTPUTS</span></span>

### <span data-ttu-id="71e3d-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="71e3d-137">System.Void</span></span>

## <span data-ttu-id="71e3d-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="71e3d-138">NOTES</span></span>

## <span data-ttu-id="71e3d-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71e3d-139">RELATED LINKS</span></span>

[<span data-ttu-id="71e3d-140">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="71e3d-140">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="71e3d-141">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="71e3d-141">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="71e3d-142">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="71e3d-142">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


