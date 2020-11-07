---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 70b92cd7762b42fba7ae890cd22b529ba80318ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697873"
---
# <span data-ttu-id="3ce7d-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3ce7d-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="3ce7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ce7d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce7d-103">자동화 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ce7d-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="3ce7d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3ce7d-104">SYNTAX</span></span>

### <span data-ttu-id="3ce7d-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="3ce7d-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ce7d-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="3ce7d-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ce7d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3ce7d-107">DESCRIPTION</span></span>
<span data-ttu-id="3ce7d-108">**AzAutomationCertificate** cmdlet은 하나 이상의 Azure 자동화 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ce7d-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="3ce7d-109">기본적으로이 cmdlet은 모든 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ce7d-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="3ce7d-110">특정 인증서를 받을 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce7d-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="3ce7d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="3ce7d-111">EXAMPLES</span></span>

### <span data-ttu-id="3ce7d-112">예제 1: 모든 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="3ce7d-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="3ce7d-113">이 명령은 Contoso17 이라는 Automation 계정의 모든 인증서에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ce7d-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="3ce7d-114">예제 2: 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="3ce7d-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="3ce7d-115">이 명령은 ContosoCertificate 이라는 인증서에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ce7d-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="3ce7d-116">변수</span><span class="sxs-lookup"><span data-stu-id="3ce7d-116">PARAMETERS</span></span>

### <span data-ttu-id="3ce7d-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3ce7d-117">-AutomationAccountName</span></span>
<span data-ttu-id="3ce7d-118">이 cmdlet이 인증서를 검색 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce7d-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="3ce7d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce7d-119">-DefaultProfile</span></span>
<span data-ttu-id="3ce7d-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3ce7d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ce7d-121">-이름</span><span class="sxs-lookup"><span data-stu-id="3ce7d-121">-Name</span></span>
<span data-ttu-id="3ce7d-122">검색할 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce7d-122">Specifies the name of a certificate to retrieve.</span></span>

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

### <span data-ttu-id="3ce7d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ce7d-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ce7d-124">이 cmdlet에서 자동화 인증서를 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce7d-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="3ce7d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce7d-125">CommonParameters</span></span>
<span data-ttu-id="3ce7d-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce7d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce7d-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce7d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce7d-128">입력</span><span class="sxs-lookup"><span data-stu-id="3ce7d-128">INPUTS</span></span>

### <span data-ttu-id="3ce7d-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3ce7d-129">System.String</span></span>

## <span data-ttu-id="3ce7d-130">출력</span><span class="sxs-lookup"><span data-stu-id="3ce7d-130">OUTPUTS</span></span>

### <span data-ttu-id="3ce7d-131">Microsoft. Azure. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="3ce7d-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="3ce7d-132">상속자</span><span class="sxs-lookup"><span data-stu-id="3ce7d-132">NOTES</span></span>

## <span data-ttu-id="3ce7d-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ce7d-133">RELATED LINKS</span></span>

[<span data-ttu-id="3ce7d-134">새로운 AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3ce7d-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="3ce7d-135">제거-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3ce7d-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="3ce7d-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3ce7d-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)

