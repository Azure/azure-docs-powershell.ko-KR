---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
ms.openlocfilehash: 1daffb4bd4c6f78c0022057faa3bef052531dd46
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492849"
---
# <span data-ttu-id="758a5-101">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="758a5-101">Remove-AzIntegrationAccount</span></span>

## <span data-ttu-id="758a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="758a5-102">SYNOPSIS</span></span>
<span data-ttu-id="758a5-103">통합 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="758a5-103">Removes an integration account.</span></span>

## <span data-ttu-id="758a5-104">구문</span><span class="sxs-lookup"><span data-stu-id="758a5-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="758a5-105">설명</span><span class="sxs-lookup"><span data-stu-id="758a5-105">DESCRIPTION</span></span>
<span data-ttu-id="758a5-106">**Remove-AzIntegrationAccount** cmdlet은 리소스 그룹에서 통합 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="758a5-106">The **Remove-AzIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="758a5-107">통합 계정 이름 및 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="758a5-107">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="758a5-108">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="758a5-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="758a5-109">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="758a5-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="758a5-110">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="758a5-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="758a5-111">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="758a5-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="758a5-112">예제</span><span class="sxs-lookup"><span data-stu-id="758a5-112">EXAMPLES</span></span>

### <span data-ttu-id="758a5-113">예제 1: 통합 계정 제거</span><span class="sxs-lookup"><span data-stu-id="758a5-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="758a5-114">이 명령은 IntegrationAccount31이라는 통합 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="758a5-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="758a5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="758a5-115">PARAMETERS</span></span>

### <span data-ttu-id="758a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="758a5-116">-DefaultProfile</span></span>
<span data-ttu-id="758a5-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="758a5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="758a5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="758a5-118">-Force</span></span>
<span data-ttu-id="758a5-119">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="758a5-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="758a5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="758a5-120">-Name</span></span>
<span data-ttu-id="758a5-121">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="758a5-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="758a5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="758a5-122">-ResourceGroupName</span></span>
<span data-ttu-id="758a5-123">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="758a5-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="758a5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="758a5-124">-Confirm</span></span>
<span data-ttu-id="758a5-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="758a5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="758a5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="758a5-126">-WhatIf</span></span>
<span data-ttu-id="758a5-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="758a5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="758a5-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="758a5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="758a5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="758a5-129">CommonParameters</span></span>
<span data-ttu-id="758a5-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="758a5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="758a5-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="758a5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="758a5-132">입력</span><span class="sxs-lookup"><span data-stu-id="758a5-132">INPUTS</span></span>

### <span data-ttu-id="758a5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="758a5-133">System.String</span></span>

## <span data-ttu-id="758a5-134">출력</span><span class="sxs-lookup"><span data-stu-id="758a5-134">OUTPUTS</span></span>

### <span data-ttu-id="758a5-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="758a5-135">System.Void</span></span>

## <span data-ttu-id="758a5-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="758a5-136">NOTES</span></span>

## <span data-ttu-id="758a5-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="758a5-137">RELATED LINKS</span></span>

[<span data-ttu-id="758a5-138">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="758a5-138">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="758a5-139">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="758a5-139">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

[<span data-ttu-id="758a5-140">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="758a5-140">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)


