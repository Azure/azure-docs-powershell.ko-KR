---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
ms.openlocfilehash: 42fc322e9f593ecad6c295952d46274eb2563799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531206"
---
# <span data-ttu-id="8500a-101">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8500a-101">Remove-AzureRmAutomationModule</span></span>

## <span data-ttu-id="8500a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8500a-102">SYNOPSIS</span></span>
<span data-ttu-id="8500a-103">자동화에서 모듈을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8500a-103">Removes a module from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8500a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8500a-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8500a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8500a-105">DESCRIPTION</span></span>
<span data-ttu-id="8500a-106">**AzureRmAutomationModule** Cmdlet은 Azure Automation의 자동화 계정에서 모듈을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8500a-106">The **Remove-AzureRmAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="8500a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8500a-107">EXAMPLES</span></span>

### <span data-ttu-id="8500a-108">예제 1: 모듈 제거</span><span class="sxs-lookup"><span data-stu-id="8500a-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8500a-109">이 명령은 Contoso17 이라는 자동화 계정에서 ContosoModule 이라는 모듈을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8500a-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8500a-110">변수</span><span class="sxs-lookup"><span data-stu-id="8500a-110">PARAMETERS</span></span>

### <span data-ttu-id="8500a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8500a-111">-AutomationAccountName</span></span>
<span data-ttu-id="8500a-112">이 cmdlet에서 모듈을 제거 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8500a-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8500a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8500a-113">-Force</span></span>
<span data-ttu-id="8500a-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="8500a-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8500a-115">-이름</span><span class="sxs-lookup"><span data-stu-id="8500a-115">-Name</span></span>
<span data-ttu-id="8500a-116">이 cmdlet이 제거 하는 모듈의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8500a-116">Specifies the name of the module that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8500a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8500a-117">-ResourceGroupName</span></span>
<span data-ttu-id="8500a-118">이 cmdlet이 모듈을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8500a-118">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8500a-119">-확인</span><span class="sxs-lookup"><span data-stu-id="8500a-119">-Confirm</span></span>
<span data-ttu-id="8500a-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8500a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8500a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8500a-121">-WhatIf</span></span>
<span data-ttu-id="8500a-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8500a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8500a-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8500a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8500a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8500a-124">-DefaultProfile</span></span>
<span data-ttu-id="8500a-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8500a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8500a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8500a-126">CommonParameters</span></span>
<span data-ttu-id="8500a-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8500a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8500a-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8500a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8500a-129">입력</span><span class="sxs-lookup"><span data-stu-id="8500a-129">INPUTS</span></span>

## <span data-ttu-id="8500a-130">출력</span><span class="sxs-lookup"><span data-stu-id="8500a-130">OUTPUTS</span></span>

## <span data-ttu-id="8500a-131">상속자</span><span class="sxs-lookup"><span data-stu-id="8500a-131">NOTES</span></span>

## <span data-ttu-id="8500a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8500a-132">RELATED LINKS</span></span>

[<span data-ttu-id="8500a-133">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8500a-133">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="8500a-134">새로운 AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8500a-134">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="8500a-135">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8500a-135">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


