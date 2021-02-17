---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
ms.openlocfilehash: e6dd090998d7a61d61fdad4bb40cbe2c62d7df1f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205528"
---
# <span data-ttu-id="0abe4-101">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0abe4-101">Remove-AzAutomationCertificate</span></span>

## <span data-ttu-id="0abe4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0abe4-102">SYNOPSIS</span></span>
<span data-ttu-id="0abe4-103">Automation 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0abe4-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="0abe4-104">구문</span><span class="sxs-lookup"><span data-stu-id="0abe4-104">SYNTAX</span></span>

```
Remove-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0abe4-105">설명</span><span class="sxs-lookup"><span data-stu-id="0abe4-105">DESCRIPTION</span></span>
<span data-ttu-id="0abe4-106">**Remove-AzAutomationCertificate** cmdlet은 Azure Automation에서 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0abe4-106">The **Remove-AzAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="0abe4-107">예제</span><span class="sxs-lookup"><span data-stu-id="0abe4-107">EXAMPLES</span></span>

### <span data-ttu-id="0abe4-108">예제 1: 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="0abe4-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0abe4-109">이 명령은 Contoso17이라는 Automation 계정에서 Cert01이라는 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0abe4-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="0abe4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0abe4-110">PARAMETERS</span></span>

### <span data-ttu-id="0abe4-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0abe4-111">-AutomationAccountName</span></span>
<span data-ttu-id="0abe4-112">이 cmdlet이 인증서를 제거하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0abe4-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="0abe4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0abe4-113">-DefaultProfile</span></span>
<span data-ttu-id="0abe4-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0abe4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0abe4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0abe4-115">-Name</span></span>
<span data-ttu-id="0abe4-116">이 cmdlet이 제거하는 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0abe4-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0abe4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0abe4-117">-ResourceGroupName</span></span>
<span data-ttu-id="0abe4-118">이 cmdlet이 인증서를 제거하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0abe4-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="0abe4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0abe4-119">-Confirm</span></span>
<span data-ttu-id="0abe4-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0abe4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0abe4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0abe4-121">-WhatIf</span></span>
<span data-ttu-id="0abe4-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0abe4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0abe4-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0abe4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0abe4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0abe4-124">CommonParameters</span></span>
<span data-ttu-id="0abe4-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0abe4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0abe4-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0abe4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0abe4-127">입력</span><span class="sxs-lookup"><span data-stu-id="0abe4-127">INPUTS</span></span>

### <span data-ttu-id="0abe4-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0abe4-128">System.String</span></span>

## <span data-ttu-id="0abe4-129">출력</span><span class="sxs-lookup"><span data-stu-id="0abe4-129">OUTPUTS</span></span>

### <span data-ttu-id="0abe4-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="0abe4-130">System.Void</span></span>

## <span data-ttu-id="0abe4-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0abe4-131">NOTES</span></span>

## <span data-ttu-id="0abe4-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0abe4-132">RELATED LINKS</span></span>

[<span data-ttu-id="0abe4-133">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0abe4-133">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="0abe4-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0abe4-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="0abe4-135">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0abe4-135">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


