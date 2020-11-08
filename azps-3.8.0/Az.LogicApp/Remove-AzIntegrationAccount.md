---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
ms.openlocfilehash: 1daffb4bd4c6f78c0022057faa3bef052531dd46
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034857"
---
# <span data-ttu-id="1df33-101">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1df33-101">Remove-AzIntegrationAccount</span></span>

## <span data-ttu-id="1df33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1df33-102">SYNOPSIS</span></span>
<span data-ttu-id="1df33-103">통합 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df33-103">Removes an integration account.</span></span>

## <span data-ttu-id="1df33-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1df33-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1df33-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1df33-105">DESCRIPTION</span></span>
<span data-ttu-id="1df33-106">**제거-AzIntegrationAccount** cmdlet은 리소스 그룹에서 통합 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df33-106">The **Remove-AzIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="1df33-107">통합 계정 이름 및 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df33-107">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="1df33-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df33-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1df33-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df33-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1df33-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df33-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1df33-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df33-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1df33-112">예제의</span><span class="sxs-lookup"><span data-stu-id="1df33-112">EXAMPLES</span></span>

### <span data-ttu-id="1df33-113">예제 1: 통합 계정 제거</span><span class="sxs-lookup"><span data-stu-id="1df33-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="1df33-114">이 명령은 IntegrationAccount31 이라는 통합 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df33-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="1df33-115">변수</span><span class="sxs-lookup"><span data-stu-id="1df33-115">PARAMETERS</span></span>

### <span data-ttu-id="1df33-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1df33-116">-DefaultProfile</span></span>
<span data-ttu-id="1df33-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1df33-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1df33-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1df33-118">-Force</span></span>
<span data-ttu-id="1df33-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df33-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1df33-120">-이름</span><span class="sxs-lookup"><span data-stu-id="1df33-120">-Name</span></span>
<span data-ttu-id="1df33-121">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df33-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="1df33-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1df33-122">-ResourceGroupName</span></span>
<span data-ttu-id="1df33-123">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df33-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1df33-124">-확인</span><span class="sxs-lookup"><span data-stu-id="1df33-124">-Confirm</span></span>
<span data-ttu-id="1df33-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df33-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1df33-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1df33-126">-WhatIf</span></span>
<span data-ttu-id="1df33-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1df33-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1df33-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1df33-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1df33-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1df33-129">CommonParameters</span></span>
<span data-ttu-id="1df33-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df33-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1df33-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1df33-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1df33-132">입력</span><span class="sxs-lookup"><span data-stu-id="1df33-132">INPUTS</span></span>

### <span data-ttu-id="1df33-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1df33-133">System.String</span></span>

## <span data-ttu-id="1df33-134">출력</span><span class="sxs-lookup"><span data-stu-id="1df33-134">OUTPUTS</span></span>

### <span data-ttu-id="1df33-135">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="1df33-135">System.Void</span></span>

## <span data-ttu-id="1df33-136">상속자</span><span class="sxs-lookup"><span data-stu-id="1df33-136">NOTES</span></span>

## <span data-ttu-id="1df33-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1df33-137">RELATED LINKS</span></span>

[<span data-ttu-id="1df33-138">새로운 AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1df33-138">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="1df33-139">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1df33-139">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

[<span data-ttu-id="1df33-140">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1df33-140">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)


