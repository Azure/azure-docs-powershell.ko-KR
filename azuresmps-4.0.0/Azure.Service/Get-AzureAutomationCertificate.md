---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FED10AA9-DD3A-4034-B78E-F9E55290B353
online version: ''
schema: 2.0.0
ms.openlocfilehash: 272969751988d3747788c2a214e8eb7ed509f232
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045663"
---
# <span data-ttu-id="0e84f-101">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0e84f-101">Get-AzureAutomationCertificate</span></span>

## <span data-ttu-id="0e84f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e84f-102">SYNOPSIS</span></span>

<span data-ttu-id="0e84f-103">Azure Automation 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e84f-103">Gets an Azure Automation certificate.</span></span>

## <span data-ttu-id="0e84f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e84f-104">SYNTAX</span></span>

### <span data-ttu-id="0e84f-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="0e84f-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCertificate -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0e84f-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="0e84f-106">ByCertificateName</span></span>
```
Get-AzureAutomationCertificate -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0e84f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0e84f-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="0e84f-108">**Get-AzureAutomationCertificate** cmdlet은 하나 이상의 Microsoft Azure Automation 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e84f-108">The **Get-AzureAutomationCertificate** cmdlet gets one or more Microsoft Azure Automation certificates.</span></span>
<span data-ttu-id="0e84f-109">기본적으로 모든 인증서가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e84f-109">By default, all certificates are returned.</span></span>
<span data-ttu-id="0e84f-110">특정 인증서를 가져오려면 해당 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e84f-110">To get a specific certificate, specify its name.</span></span>

## <span data-ttu-id="0e84f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="0e84f-111">EXAMPLES</span></span>

### <span data-ttu-id="0e84f-112">예제 1: 모든 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="0e84f-112">Example 1: Get all certificates</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17"
```

<span data-ttu-id="0e84f-113">이 명령은 Contoso17 이라는 Azure Automation 계정의 모든 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e84f-113">This command gets all certificates in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="0e84f-114">예제 2: 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="0e84f-114">Example 2: Get a certificate</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyUserCertificate"
```

<span data-ttu-id="0e84f-115">이 명령은 MyUserCertificate 이라는 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e84f-115">This command gets the certificate named MyUserCertificate.</span></span>

## <span data-ttu-id="0e84f-116">변수</span><span class="sxs-lookup"><span data-stu-id="0e84f-116">PARAMETERS</span></span>

### <span data-ttu-id="0e84f-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0e84f-117">-AutomationAccountName</span></span>
<span data-ttu-id="0e84f-118">인증서를 사용 하 여 automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e84f-118">Specifies the name of the automation account with the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e84f-119">-이름</span><span class="sxs-lookup"><span data-stu-id="0e84f-119">-Name</span></span>
<span data-ttu-id="0e84f-120">검색할 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e84f-120">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e84f-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="0e84f-121">-Profile</span></span>
<span data-ttu-id="0e84f-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e84f-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0e84f-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="0e84f-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e84f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e84f-124">CommonParameters</span></span>
<span data-ttu-id="0e84f-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e84f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e84f-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e84f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e84f-127">입력</span><span class="sxs-lookup"><span data-stu-id="0e84f-127">INPUTS</span></span>

## <span data-ttu-id="0e84f-128">출력</span><span class="sxs-lookup"><span data-stu-id="0e84f-128">OUTPUTS</span></span>

### <span data-ttu-id="0e84f-129">Microsoft. Azure. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="0e84f-129">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="0e84f-130">상속자</span><span class="sxs-lookup"><span data-stu-id="0e84f-130">NOTES</span></span>

## <span data-ttu-id="0e84f-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e84f-131">RELATED LINKS</span></span>

[<span data-ttu-id="0e84f-132">새-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0e84f-132">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="0e84f-133">-AzureAutomationCertificate 제거</span><span class="sxs-lookup"><span data-stu-id="0e84f-133">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="0e84f-134">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0e84f-134">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


