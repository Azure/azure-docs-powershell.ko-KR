---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: AE74024A-A12A-4EC4-AF6C-62F921EA2532
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b19d0bb0c95e9d489fe26c1cd74705318cedcf2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046428"
---
# <span data-ttu-id="06c8f-101">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="06c8f-101">Set-AzureAutomationCertificate</span></span>

## <span data-ttu-id="06c8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06c8f-102">SYNOPSIS</span></span>

<span data-ttu-id="06c8f-103">자동화 인증서의 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c8f-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="06c8f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06c8f-104">SYNTAX</span></span>

```
Set-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="06c8f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="06c8f-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="06c8f-106">**Set AzureAutomationCertificate** Cmdlet은 Microsoft Azure Automation의 인증서 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c8f-106">The **Set-AzureAutomationCertificate** cmdlet modifies the configuration of a certificate in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="06c8f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="06c8f-107">EXAMPLES</span></span>

### <span data-ttu-id="06c8f-108">예제 1: 인증서 업데이트</span><span class="sxs-lookup"><span data-stu-id="06c8f-108">Example 1: Update a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="06c8f-109">이러한 명령은 자동으로 MyCertificate 라는 기존 인증서를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c8f-109">These commands update an existing certificate named MyCertificate in Automation.</span></span>
<span data-ttu-id="06c8f-110">첫 번째 명령은 인증서를 업데이트 하는 두 번째 명령에 사용 되는 인증서 파일에 대 한 암호를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="06c8f-110">The first command creates the password for the certificate file that is used in the second command that updates the certificate.</span></span>

## <span data-ttu-id="06c8f-111">변수</span><span class="sxs-lookup"><span data-stu-id="06c8f-111">PARAMETERS</span></span>

### <span data-ttu-id="06c8f-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="06c8f-112">-AutomationAccountName</span></span>
<span data-ttu-id="06c8f-113">인증서를 사용 하 여 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c8f-113">Specifies the name of the Automation account with the certificate.</span></span>

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

### <span data-ttu-id="06c8f-114">-설명</span><span class="sxs-lookup"><span data-stu-id="06c8f-114">-Description</span></span>
<span data-ttu-id="06c8f-115">인증서에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c8f-115">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="06c8f-116">-내보내기 가능한</span><span class="sxs-lookup"><span data-stu-id="06c8f-116">-Exportable</span></span>
<span data-ttu-id="06c8f-117">인증서를 내보낼 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="06c8f-117">Indicates the certificate can be exported.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06c8f-118">-이름</span><span class="sxs-lookup"><span data-stu-id="06c8f-118">-Name</span></span>
<span data-ttu-id="06c8f-119">인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c8f-119">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="06c8f-120">-암호</span><span class="sxs-lookup"><span data-stu-id="06c8f-120">-Password</span></span>
<span data-ttu-id="06c8f-121">인증서 파일에 대 한 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c8f-121">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="06c8f-122">-Path</span><span class="sxs-lookup"><span data-stu-id="06c8f-122">-Path</span></span>
<span data-ttu-id="06c8f-123">업로드할 스크립트 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c8f-123">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="06c8f-124">파일은 .cer 또는 .pfx 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06c8f-124">The file can be .cer or .pfx.</span></span>

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

### <span data-ttu-id="06c8f-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="06c8f-125">-Profile</span></span>
<span data-ttu-id="06c8f-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c8f-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="06c8f-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="06c8f-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="06c8f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06c8f-128">CommonParameters</span></span>
<span data-ttu-id="06c8f-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c8f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06c8f-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06c8f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06c8f-131">입력</span><span class="sxs-lookup"><span data-stu-id="06c8f-131">INPUTS</span></span>

## <span data-ttu-id="06c8f-132">출력</span><span class="sxs-lookup"><span data-stu-id="06c8f-132">OUTPUTS</span></span>

### <span data-ttu-id="06c8f-133">Microsoft. Azure. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="06c8f-133">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="06c8f-134">상속자</span><span class="sxs-lookup"><span data-stu-id="06c8f-134">NOTES</span></span>

## <span data-ttu-id="06c8f-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06c8f-135">RELATED LINKS</span></span>

[<span data-ttu-id="06c8f-136">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="06c8f-136">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="06c8f-137">새-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="06c8f-137">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="06c8f-138">-AzureAutomationCertificate 제거</span><span class="sxs-lookup"><span data-stu-id="06c8f-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)


