---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
ms.openlocfilehash: 956569d407918d0891af6aa1d6f8f09eb61b9a98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710995"
---
# <span data-ttu-id="1033b-101">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1033b-101">Get-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="1033b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1033b-102">SYNOPSIS</span></span>
<span data-ttu-id="1033b-103">자동화 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1033b-103">Gets Automation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1033b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1033b-104">SYNTAX</span></span>

### <span data-ttu-id="1033b-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="1033b-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1033b-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="1033b-106">ByCertificateName</span></span>
```
Get-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1033b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1033b-107">DESCRIPTION</span></span>
<span data-ttu-id="1033b-108">**AzureRmAutomationCertificate** cmdlet은 하나 이상의 Azure 자동화 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1033b-108">The **Get-AzureRmAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="1033b-109">기본적으로이 cmdlet은 모든 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1033b-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="1033b-110">특정 인증서를 받을 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1033b-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="1033b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1033b-111">EXAMPLES</span></span>

### <span data-ttu-id="1033b-112">예제 1: 모든 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="1033b-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="1033b-113">이 명령은 Contoso17 이라는 Automation 계정의 모든 인증서에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1033b-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="1033b-114">예제 2: 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="1033b-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="1033b-115">이 명령은 ContosoCertificate 이라는 인증서에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1033b-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="1033b-116">변수</span><span class="sxs-lookup"><span data-stu-id="1033b-116">PARAMETERS</span></span>

### <span data-ttu-id="1033b-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1033b-117">-AutomationAccountName</span></span>
<span data-ttu-id="1033b-118">이 cmdlet이 인증서를 검색 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1033b-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="1033b-119">-이름</span><span class="sxs-lookup"><span data-stu-id="1033b-119">-Name</span></span>
<span data-ttu-id="1033b-120">검색할 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1033b-120">Specifies the name of a certificate to retrieve.</span></span>

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

### <span data-ttu-id="1033b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1033b-121">-ResourceGroupName</span></span>
<span data-ttu-id="1033b-122">이 cmdlet에서 자동화 인증서를 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1033b-122">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="1033b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1033b-123">-DefaultProfile</span></span>
<span data-ttu-id="1033b-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1033b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1033b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1033b-125">CommonParameters</span></span>
<span data-ttu-id="1033b-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1033b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1033b-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1033b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1033b-128">입력</span><span class="sxs-lookup"><span data-stu-id="1033b-128">INPUTS</span></span>

## <span data-ttu-id="1033b-129">출력</span><span class="sxs-lookup"><span data-stu-id="1033b-129">OUTPUTS</span></span>

### <span data-ttu-id="1033b-130">Microsoft. Azure. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="1033b-130">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="1033b-131">상속자</span><span class="sxs-lookup"><span data-stu-id="1033b-131">NOTES</span></span>

## <span data-ttu-id="1033b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1033b-132">RELATED LINKS</span></span>

[<span data-ttu-id="1033b-133">새로운 AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1033b-133">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="1033b-134">제거-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1033b-134">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="1033b-135">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1033b-135">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


