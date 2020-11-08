---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A6D5C40-2532-4FD1-A74F-16725CAD8EDD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29d049dbdce93102411a875cfaef8e5fb9c719b6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046395"
---
# <span data-ttu-id="b8d4b-101">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="b8d4b-101">Add-AzureCertificate</span></span>

## <span data-ttu-id="b8d4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d4b-103">Azure 클라우드 서비스에 인증서를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-103">Uploads a certificate to an Azure cloud service.</span></span>

## <span data-ttu-id="b8d4b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8d4b-104">SYNTAX</span></span>

```
Add-AzureCertificate [-ServiceName] <String> [-CertToDeploy] <Object> [-Password <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8d4b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b8d4b-105">DESCRIPTION</span></span>
<span data-ttu-id="b8d4b-106">**추가-AzureCertificate** Cmdlet은 Azure 서비스에 대 한 인증서를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-106">The **Add-AzureCertificate** cmdlet uploads a certificate for an Azure service.</span></span>

## <span data-ttu-id="b8d4b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b8d4b-107">EXAMPLES</span></span>

### <span data-ttu-id="b8d4b-108">예제 1: 인증서 및 암호 업로드</span><span class="sxs-lookup"><span data-stu-id="b8d4b-108">Example 1: Upload a certificate and password</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy ContosoCertificate.pfx -Password "password"
```

<span data-ttu-id="b8d4b-109">이 명령은 ContosoCertificate 인증서 파일을 클라우드 서비스에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-109">This command uploads the certificate file ContosoCertificate.pfx to a cloud service.</span></span>
<span data-ttu-id="b8d4b-110">명령은 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-110">The command specifies the password for the certificate.</span></span>

### <span data-ttu-id="b8d4b-111">예제 2: 인증서 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="b8d4b-111">Example 2: Upload a certificate file</span></span>
```
PS C:\> Add-AzureCertificate -serviceName "MyService" -CertToDeploy ContosoCertificate.cer
```

<span data-ttu-id="b8d4b-112">이 명령은 인증서 파일 ContosoCertificate을 클라우드 서비스에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-112">This command uploads the certificate file ContosoCertificate.cer to a cloud service.</span></span>
<span data-ttu-id="b8d4b-113">명령은 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-113">The command specifies the password for the certificate.</span></span>

### <span data-ttu-id="b8d4b-114">예제 3: 인증서 개체 업로드</span><span class="sxs-lookup"><span data-stu-id="b8d4b-114">Example 3: Upload a certificate object</span></span>
```
PS C:\> $Certificate = Get-Item cert:\PATTIFULLER\MY\1D6E34B526723E06C235BE8E5457784BF12C9F39
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy $Certificate
```

<span data-ttu-id="b8d4b-115">첫 번째 명령은 Windows PowerShell core **Get 항목** cmdlet을 사용 하 여 사용자의 MY store에서 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-115">The first command gets a certificate from the MY store of a user by using the Windows PowerShell core **Get-Item** cmdlet.</span></span>
<span data-ttu-id="b8d4b-116">명령이 $Certificate 변수에 인증서를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-116">The command stores the certificate in the $Certificate variable.</span></span>

<span data-ttu-id="b8d4b-117">두 번째 명령은 $certificate의 인증서를 클라우드 서비스에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-117">The second command uploads the certificate in $certificate to a cloud service.</span></span>

## <span data-ttu-id="b8d4b-118">변수</span><span class="sxs-lookup"><span data-stu-id="b8d4b-118">PARAMETERS</span></span>

### <span data-ttu-id="b8d4b-119">-CertToDeploy</span><span class="sxs-lookup"><span data-stu-id="b8d4b-119">-CertToDeploy</span></span>
<span data-ttu-id="b8d4b-120">배포할 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-120">Specifies the certificate to deploy.</span></span>
<span data-ttu-id="b8d4b-121">\* .Cer 또는 \* 파일이 있는 파일과 같은 인증서 파일의 전체 경로를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-121">You can specify the full path of a certificate file, such as a file that has a \*.cer or \*.</span></span>
<span data-ttu-id="b8d4b-122">pfx 파일 이름 확장명 또는 X. x.509 Certificate 개체.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-122">pfx file name extension, or an X.509 Certificate object.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d4b-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b8d4b-123">-InformationAction</span></span>
<span data-ttu-id="b8d4b-124">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b8d4b-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8d4b-126">하기로</span><span class="sxs-lookup"><span data-stu-id="b8d4b-126">Continue</span></span>
- <span data-ttu-id="b8d4b-127">숨기기</span><span class="sxs-lookup"><span data-stu-id="b8d4b-127">Ignore</span></span>
- <span data-ttu-id="b8d4b-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="b8d4b-128">Inquire</span></span>
- <span data-ttu-id="b8d4b-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b8d4b-129">SilentlyContinue</span></span>
- <span data-ttu-id="b8d4b-130">중지가</span><span class="sxs-lookup"><span data-stu-id="b8d4b-130">Stop</span></span>
- <span data-ttu-id="b8d4b-131">대기</span><span class="sxs-lookup"><span data-stu-id="b8d4b-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d4b-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b8d4b-132">-InformationVariable</span></span>
<span data-ttu-id="b8d4b-133">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d4b-134">-암호</span><span class="sxs-lookup"><span data-stu-id="b8d4b-134">-Password</span></span>
<span data-ttu-id="b8d4b-135">인증서 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-135">Specifies the certificate password.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d4b-136">-프로필</span><span class="sxs-lookup"><span data-stu-id="b8d4b-136">-Profile</span></span>
<span data-ttu-id="b8d4b-137">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b8d4b-138">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b8d4b-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b8d4b-139">-ServiceName</span></span>
<span data-ttu-id="b8d4b-140">이 cmdlet이 인증서를 추가 하는 Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-140">Specifies the name of the Azure service to which this cmdlet adds a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d4b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d4b-141">CommonParameters</span></span>
<span data-ttu-id="b8d4b-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d4b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d4b-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8d4b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d4b-144">입력</span><span class="sxs-lookup"><span data-stu-id="b8d4b-144">INPUTS</span></span>

## <span data-ttu-id="b8d4b-145">출력</span><span class="sxs-lookup"><span data-stu-id="b8d4b-145">OUTPUTS</span></span>

### <span data-ttu-id="b8d4b-146">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="b8d4b-146">ManagementOperationContext</span></span>

## <span data-ttu-id="b8d4b-147">상속자</span><span class="sxs-lookup"><span data-stu-id="b8d4b-147">NOTES</span></span>

## <span data-ttu-id="b8d4b-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8d4b-148">RELATED LINKS</span></span>

[<span data-ttu-id="b8d4b-149">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="b8d4b-149">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="b8d4b-150">새로운 AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="b8d4b-150">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)

[<span data-ttu-id="b8d4b-151">제거-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="b8d4b-151">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


