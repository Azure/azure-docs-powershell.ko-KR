---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
ms.openlocfilehash: e6dd090998d7a61d61fdad4bb40cbe2c62d7df1f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056804"
---
# <span data-ttu-id="01423-101">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="01423-101">Remove-AzAutomationCertificate</span></span>

## <span data-ttu-id="01423-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01423-102">SYNOPSIS</span></span>
<span data-ttu-id="01423-103">자동화 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="01423-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="01423-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01423-104">SYNTAX</span></span>

```
Remove-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01423-105">설명은</span><span class="sxs-lookup"><span data-stu-id="01423-105">DESCRIPTION</span></span>
<span data-ttu-id="01423-106">**AzAutomationCertificate** Cmdlet은 Azure Automation에서 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="01423-106">The **Remove-AzAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="01423-107">예제의</span><span class="sxs-lookup"><span data-stu-id="01423-107">EXAMPLES</span></span>

### <span data-ttu-id="01423-108">예제 1: 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="01423-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="01423-109">이 명령은 Contoso17 이라는 Automation 계정에서 Cert01 이라는 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="01423-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="01423-110">변수</span><span class="sxs-lookup"><span data-stu-id="01423-110">PARAMETERS</span></span>

### <span data-ttu-id="01423-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="01423-111">-AutomationAccountName</span></span>
<span data-ttu-id="01423-112">이 cmdlet이 인증서를 제거 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01423-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="01423-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01423-113">-DefaultProfile</span></span>
<span data-ttu-id="01423-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="01423-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01423-115">-이름</span><span class="sxs-lookup"><span data-stu-id="01423-115">-Name</span></span>
<span data-ttu-id="01423-116">이 cmdlet이 제거할 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01423-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="01423-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01423-117">-ResourceGroupName</span></span>
<span data-ttu-id="01423-118">이 cmdlet이 인증서를 제거할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01423-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="01423-119">-확인</span><span class="sxs-lookup"><span data-stu-id="01423-119">-Confirm</span></span>
<span data-ttu-id="01423-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="01423-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01423-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01423-121">-WhatIf</span></span>
<span data-ttu-id="01423-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="01423-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01423-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01423-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01423-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01423-124">CommonParameters</span></span>
<span data-ttu-id="01423-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01423-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01423-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01423-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01423-127">입력</span><span class="sxs-lookup"><span data-stu-id="01423-127">INPUTS</span></span>

### <span data-ttu-id="01423-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="01423-128">System.String</span></span>

## <span data-ttu-id="01423-129">출력</span><span class="sxs-lookup"><span data-stu-id="01423-129">OUTPUTS</span></span>

### <span data-ttu-id="01423-130">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="01423-130">System.Void</span></span>

## <span data-ttu-id="01423-131">상속자</span><span class="sxs-lookup"><span data-stu-id="01423-131">NOTES</span></span>

## <span data-ttu-id="01423-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01423-132">RELATED LINKS</span></span>

[<span data-ttu-id="01423-133">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="01423-133">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="01423-134">새로운 AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="01423-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="01423-135">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="01423-135">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


