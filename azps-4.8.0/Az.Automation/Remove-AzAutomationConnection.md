---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 1beda1b4db41c2aa3bf40bba7b72e0e684ba3196
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048516"
---
# <span data-ttu-id="0ae00-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="0ae00-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="0ae00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ae00-102">SYNOPSIS</span></span>
<span data-ttu-id="0ae00-103">자동화 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae00-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="0ae00-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ae00-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ae00-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0ae00-105">DESCRIPTION</span></span>
<span data-ttu-id="0ae00-106">**AzAutomationConnection** Cmdlet은 Azure Automation에서 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae00-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="0ae00-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0ae00-107">EXAMPLES</span></span>

### <span data-ttu-id="0ae00-108">예제 1: 연결 제거</span><span class="sxs-lookup"><span data-stu-id="0ae00-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0ae00-109">이 명령은 Contoso17 이라는 Automation 계정에서 ContosoConnection 이라는 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae00-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="0ae00-110">변수</span><span class="sxs-lookup"><span data-stu-id="0ae00-110">PARAMETERS</span></span>

### <span data-ttu-id="0ae00-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0ae00-111">-AutomationAccountName</span></span>
<span data-ttu-id="0ae00-112">이 cmdlet이 연결을 제거 하는 automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae00-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="0ae00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ae00-113">-DefaultProfile</span></span>
<span data-ttu-id="0ae00-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0ae00-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ae00-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0ae00-115">-Force</span></span>
<span data-ttu-id="0ae00-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="0ae00-116">ps_force</span></span>

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

### <span data-ttu-id="0ae00-117">-이름</span><span class="sxs-lookup"><span data-stu-id="0ae00-117">-Name</span></span>
<span data-ttu-id="0ae00-118">이 cmdlet이 제거 하는 연결의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae00-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0ae00-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ae00-119">-ResourceGroupName</span></span>
<span data-ttu-id="0ae00-120">이 cmdlet이 연결을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae00-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="0ae00-121">-확인</span><span class="sxs-lookup"><span data-stu-id="0ae00-121">-Confirm</span></span>
<span data-ttu-id="0ae00-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae00-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ae00-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ae00-123">-WhatIf</span></span>
<span data-ttu-id="0ae00-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0ae00-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ae00-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ae00-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ae00-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ae00-126">CommonParameters</span></span>
<span data-ttu-id="0ae00-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae00-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ae00-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ae00-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ae00-129">입력</span><span class="sxs-lookup"><span data-stu-id="0ae00-129">INPUTS</span></span>

### <span data-ttu-id="0ae00-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0ae00-130">System.String</span></span>

## <span data-ttu-id="0ae00-131">출력</span><span class="sxs-lookup"><span data-stu-id="0ae00-131">OUTPUTS</span></span>

### <span data-ttu-id="0ae00-132">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="0ae00-132">System.Void</span></span>

## <span data-ttu-id="0ae00-133">상속자</span><span class="sxs-lookup"><span data-stu-id="0ae00-133">NOTES</span></span>

## <span data-ttu-id="0ae00-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ae00-134">RELATED LINKS</span></span>

[<span data-ttu-id="0ae00-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="0ae00-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="0ae00-136">새로운 AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="0ae00-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


