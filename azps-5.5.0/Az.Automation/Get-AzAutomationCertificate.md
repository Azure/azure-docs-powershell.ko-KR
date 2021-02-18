---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 3a504ba081852ff3bb84a6ace432b394a2b2b478
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201228"
---
# <span data-ttu-id="e8a9f-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e8a9f-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="e8a9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8a9f-102">SYNOPSIS</span></span>
<span data-ttu-id="e8a9f-103">Automation 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e8a9f-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="e8a9f-104">구문</span><span class="sxs-lookup"><span data-stu-id="e8a9f-104">SYNTAX</span></span>

### <span data-ttu-id="e8a9f-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="e8a9f-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8a9f-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="e8a9f-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8a9f-107">설명</span><span class="sxs-lookup"><span data-stu-id="e8a9f-107">DESCRIPTION</span></span>
<span data-ttu-id="e8a9f-108">**Get-AzAutomationCertificate** cmdlet은 하나 이상의 Azure Automation 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e8a9f-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="e8a9f-109">기본적으로 이 cmdlet은 모든 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e8a9f-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="e8a9f-110">특정 인증서를 얻을 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a9f-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="e8a9f-111">예제</span><span class="sxs-lookup"><span data-stu-id="e8a9f-111">EXAMPLES</span></span>

### <span data-ttu-id="e8a9f-112">예제 1: 모든 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e8a9f-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="e8a9f-113">이 명령은 Contoso17이라는 Automation 계정의 모든 인증서에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e8a9f-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="e8a9f-114">예제 2: 인증서 얻기</span><span class="sxs-lookup"><span data-stu-id="e8a9f-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="e8a9f-115">이 명령은 ContosoCertificate라는 인증서에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e8a9f-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="e8a9f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8a9f-116">PARAMETERS</span></span>

### <span data-ttu-id="e8a9f-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e8a9f-117">-AutomationAccountName</span></span>
<span data-ttu-id="e8a9f-118">이 cmdlet이 인증서를 검색하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a9f-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="e8a9f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8a9f-119">-DefaultProfile</span></span>
<span data-ttu-id="e8a9f-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e8a9f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8a9f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e8a9f-121">-Name</span></span>
<span data-ttu-id="e8a9f-122">검색할 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a9f-122">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8a9f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8a9f-123">-ResourceGroupName</span></span>
<span data-ttu-id="e8a9f-124">이 cmdlet이 Automation 인증서를 받을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a9f-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="e8a9f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8a9f-125">CommonParameters</span></span>
<span data-ttu-id="e8a9f-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a9f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8a9f-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8a9f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8a9f-128">입력</span><span class="sxs-lookup"><span data-stu-id="e8a9f-128">INPUTS</span></span>

### <span data-ttu-id="e8a9f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e8a9f-129">System.String</span></span>

## <span data-ttu-id="e8a9f-130">출력</span><span class="sxs-lookup"><span data-stu-id="e8a9f-130">OUTPUTS</span></span>

### <span data-ttu-id="e8a9f-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="e8a9f-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="e8a9f-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e8a9f-132">NOTES</span></span>

## <span data-ttu-id="e8a9f-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8a9f-133">RELATED LINKS</span></span>

[<span data-ttu-id="e8a9f-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e8a9f-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="e8a9f-135">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e8a9f-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="e8a9f-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e8a9f-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


