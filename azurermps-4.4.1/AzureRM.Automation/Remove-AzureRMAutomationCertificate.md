---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
ms.openlocfilehash: d1230030f95d22d972aa537208b30f350ec9dbe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531861"
---
# <span data-ttu-id="ce12d-101">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce12d-101">Remove-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="ce12d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce12d-102">SYNOPSIS</span></span>
<span data-ttu-id="ce12d-103">자동화 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce12d-103">Removes an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce12d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ce12d-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce12d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ce12d-105">DESCRIPTION</span></span>
<span data-ttu-id="ce12d-106">**AzureRmAutomationCertificate** Cmdlet은 Azure Automation에서 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce12d-106">The **Remove-AzureRmAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="ce12d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ce12d-107">EXAMPLES</span></span>

### <span data-ttu-id="ce12d-108">예제 1: 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="ce12d-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ce12d-109">이 명령은 Contoso17 이라는 Automation 계정에서 Cert01 이라는 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce12d-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="ce12d-110">변수</span><span class="sxs-lookup"><span data-stu-id="ce12d-110">PARAMETERS</span></span>

### <span data-ttu-id="ce12d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ce12d-111">-AutomationAccountName</span></span>
<span data-ttu-id="ce12d-112">이 cmdlet이 인증서를 제거 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce12d-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="ce12d-113">-이름</span><span class="sxs-lookup"><span data-stu-id="ce12d-113">-Name</span></span>
<span data-ttu-id="ce12d-114">이 cmdlet이 제거할 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce12d-114">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ce12d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce12d-115">-ResourceGroupName</span></span>
<span data-ttu-id="ce12d-116">이 cmdlet이 인증서를 제거할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce12d-116">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="ce12d-117">-확인</span><span class="sxs-lookup"><span data-stu-id="ce12d-117">-Confirm</span></span>
<span data-ttu-id="ce12d-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce12d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce12d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce12d-119">-WhatIf</span></span>
<span data-ttu-id="ce12d-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce12d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce12d-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce12d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce12d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce12d-122">-DefaultProfile</span></span>
<span data-ttu-id="ce12d-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce12d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce12d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce12d-124">CommonParameters</span></span>
<span data-ttu-id="ce12d-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce12d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce12d-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce12d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce12d-127">입력</span><span class="sxs-lookup"><span data-stu-id="ce12d-127">INPUTS</span></span>

## <span data-ttu-id="ce12d-128">출력</span><span class="sxs-lookup"><span data-stu-id="ce12d-128">OUTPUTS</span></span>

## <span data-ttu-id="ce12d-129">상속자</span><span class="sxs-lookup"><span data-stu-id="ce12d-129">NOTES</span></span>

## <span data-ttu-id="ce12d-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce12d-130">RELATED LINKS</span></span>

[<span data-ttu-id="ce12d-131">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce12d-131">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="ce12d-132">새로운 AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce12d-132">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="ce12d-133">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce12d-133">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


