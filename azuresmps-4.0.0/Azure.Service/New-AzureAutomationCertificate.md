---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FDA8BAAA-7C37-4BCB-9C02-EB6296C09C2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 00904cc1b67c32bc3658c1c4f6e8b123a5601ff7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046222"
---
# <span data-ttu-id="086f0-101">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="086f0-101">New-AzureAutomationCertificate</span></span>

## <span data-ttu-id="086f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="086f0-102">SYNOPSIS</span></span>

<span data-ttu-id="086f0-103">Azure Automation 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="086f0-103">Creates an Azure Automation certificate.</span></span>

## <span data-ttu-id="086f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="086f0-104">SYNTAX</span></span>

```
New-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>] -Path <String>
 [-Exportable] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="086f0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="086f0-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="086f0-106">**새로운-AzureAutomationCertificate** Cmdlet은 Microsoft Azure 자동화에 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="086f0-106">The **New-AzureAutomationCertificate** cmdlet creates a certificate in Microsoft Azure Automation.</span></span>
<span data-ttu-id="086f0-107">업로드할 인증서 파일에 대 한 경로를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="086f0-107">You provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="086f0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="086f0-108">EXAMPLES</span></span>

### <span data-ttu-id="086f0-109">예제 1: 인증서 만들기</span><span class="sxs-lookup"><span data-stu-id="086f0-109">Example 1: Create a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> New-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="086f0-110">이러한 명령은 MyCertificate 라는 Azure Automation에서 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="086f0-110">These commands create a certificate in Azure Automation named MyCertificate.</span></span>
<span data-ttu-id="086f0-111">첫 번째 명령은 인증서를 만드는 두 번째 명령에 사용 되는 인증서 파일에 대 한 암호를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="086f0-111">The first command creates the password for the certificate file that is used in the second command that creates the certificate.</span></span>

## <span data-ttu-id="086f0-112">변수</span><span class="sxs-lookup"><span data-stu-id="086f0-112">PARAMETERS</span></span>

### <span data-ttu-id="086f0-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="086f0-113">-AutomationAccountName</span></span>
<span data-ttu-id="086f0-114">인증서를 저장할 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="086f0-114">Specifies the name of the Automation account the certificate will be stored in.</span></span>

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

### <span data-ttu-id="086f0-115">-설명</span><span class="sxs-lookup"><span data-stu-id="086f0-115">-Description</span></span>
<span data-ttu-id="086f0-116">인증서에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="086f0-116">Specifies a description for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="086f0-117">-내보내기 가능한</span><span class="sxs-lookup"><span data-stu-id="086f0-117">-Exportable</span></span>
<span data-ttu-id="086f0-118">인증서를 내보낼 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="086f0-118">Indicates the certificate can be exported.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="086f0-119">-이름</span><span class="sxs-lookup"><span data-stu-id="086f0-119">-Name</span></span>
<span data-ttu-id="086f0-120">인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="086f0-120">Specifies a name for the certificate.</span></span>

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

### <span data-ttu-id="086f0-121">-암호</span><span class="sxs-lookup"><span data-stu-id="086f0-121">-Password</span></span>
<span data-ttu-id="086f0-122">인증서 파일에 대 한 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="086f0-122">Specifies the password for the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="086f0-123">-Path</span><span class="sxs-lookup"><span data-stu-id="086f0-123">-Path</span></span>
<span data-ttu-id="086f0-124">업로드할 스크립트 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="086f0-124">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="086f0-125">파일은 .cer 또는 .pfx 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="086f0-125">The file can be .cer or .pfx.</span></span>

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

### <span data-ttu-id="086f0-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="086f0-126">-Profile</span></span>
<span data-ttu-id="086f0-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="086f0-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="086f0-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="086f0-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="086f0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="086f0-129">CommonParameters</span></span>
<span data-ttu-id="086f0-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="086f0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="086f0-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="086f0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="086f0-132">입력</span><span class="sxs-lookup"><span data-stu-id="086f0-132">INPUTS</span></span>

## <span data-ttu-id="086f0-133">출력</span><span class="sxs-lookup"><span data-stu-id="086f0-133">OUTPUTS</span></span>

### <span data-ttu-id="086f0-134">Microsoft. Azure. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="086f0-134">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="086f0-135">상속자</span><span class="sxs-lookup"><span data-stu-id="086f0-135">NOTES</span></span>

## <span data-ttu-id="086f0-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="086f0-136">RELATED LINKS</span></span>

[<span data-ttu-id="086f0-137">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="086f0-137">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="086f0-138">-AzureAutomationCertificate 제거</span><span class="sxs-lookup"><span data-stu-id="086f0-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="086f0-139">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="086f0-139">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


