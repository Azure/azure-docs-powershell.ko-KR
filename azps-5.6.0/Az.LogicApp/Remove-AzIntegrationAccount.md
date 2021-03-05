---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
ms.openlocfilehash: d1f15544223a20113a40975780aa8ca899205f7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962000"
---
# <span data-ttu-id="7d23d-101">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="7d23d-101">Remove-AzIntegrationAccount</span></span>

## <span data-ttu-id="7d23d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d23d-102">SYNOPSIS</span></span>
<span data-ttu-id="7d23d-103">통합 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7d23d-103">Removes an integration account.</span></span>

## <span data-ttu-id="7d23d-104">구문</span><span class="sxs-lookup"><span data-stu-id="7d23d-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d23d-105">설명</span><span class="sxs-lookup"><span data-stu-id="7d23d-105">DESCRIPTION</span></span>
<span data-ttu-id="7d23d-106">**Remove-AzIntegrationAccount** cmdlet은 리소스 그룹에서 통합 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7d23d-106">The **Remove-AzIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="7d23d-107">통합 계정 이름 및 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d23d-107">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="7d23d-108">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7d23d-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7d23d-109">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d23d-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7d23d-110">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 뒤 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="7d23d-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7d23d-111">필요한 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d23d-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7d23d-112">예제</span><span class="sxs-lookup"><span data-stu-id="7d23d-112">EXAMPLES</span></span>

### <span data-ttu-id="7d23d-113">예제 1: 통합 계정 제거</span><span class="sxs-lookup"><span data-stu-id="7d23d-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="7d23d-114">이 명령은 IntegrationAccount31이라는 통합 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7d23d-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="7d23d-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7d23d-115">PARAMETERS</span></span>

### <span data-ttu-id="7d23d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d23d-116">-DefaultProfile</span></span>
<span data-ttu-id="7d23d-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7d23d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d23d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7d23d-118">-Force</span></span>
<span data-ttu-id="7d23d-119">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7d23d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7d23d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7d23d-120">-Name</span></span>
<span data-ttu-id="7d23d-121">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d23d-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="7d23d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d23d-122">-ResourceGroupName</span></span>
<span data-ttu-id="7d23d-123">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d23d-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7d23d-124">-확인</span><span class="sxs-lookup"><span data-stu-id="7d23d-124">-Confirm</span></span>
<span data-ttu-id="7d23d-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d23d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d23d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d23d-126">-WhatIf</span></span>
<span data-ttu-id="7d23d-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7d23d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d23d-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d23d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d23d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d23d-129">CommonParameters</span></span>
<span data-ttu-id="7d23d-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7d23d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d23d-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7d23d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d23d-132">입력</span><span class="sxs-lookup"><span data-stu-id="7d23d-132">INPUTS</span></span>

### <span data-ttu-id="7d23d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7d23d-133">System.String</span></span>

## <span data-ttu-id="7d23d-134">출력</span><span class="sxs-lookup"><span data-stu-id="7d23d-134">OUTPUTS</span></span>

### <span data-ttu-id="7d23d-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="7d23d-135">System.Void</span></span>

## <span data-ttu-id="7d23d-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7d23d-136">NOTES</span></span>

## <span data-ttu-id="7d23d-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d23d-137">RELATED LINKS</span></span>

[<span data-ttu-id="7d23d-138">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="7d23d-138">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="7d23d-139">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="7d23d-139">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

[<span data-ttu-id="7d23d-140">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="7d23d-140">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)


