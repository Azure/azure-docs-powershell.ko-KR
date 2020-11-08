---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 350638E1-636E-484B-88EB-91F48129D80B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c665288d12897e4ab7277dd4ccf4bc5d975c037
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046048"
---
# <span data-ttu-id="4876f-101">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="4876f-101">Set-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="4876f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4876f-102">SYNOPSIS</span></span>
<span data-ttu-id="4876f-103">클라우드 서비스에 대 한 AD 도메인 확장을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-103">Enables an AD Domain extension for a cloud service.</span></span>

## <span data-ttu-id="4876f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4876f-104">SYNTAX</span></span>

### <span data-ttu-id="4876f-105">JoinDomainUsingEnumOptions (기본값)</span><span class="sxs-lookup"><span data-stu-id="4876f-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4876f-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="4876f-106">JoinDomainUsingJoinOption</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4876f-107">근무 그룹</span><span class="sxs-lookup"><span data-stu-id="4876f-107">WorkGroupName</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4876f-108">JoinDomainUsingEnumOptionsAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="4876f-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4876f-109">JoinDomainUsingJoinOptionAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="4876f-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4876f-110">WorkGroupNameThumbprint</span><span class="sxs-lookup"><span data-stu-id="4876f-110">WorkGroupNameThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4876f-111">설명은</span><span class="sxs-lookup"><span data-stu-id="4876f-111">DESCRIPTION</span></span>
<span data-ttu-id="4876f-112">**Set-AzureServiceADDomainExtension** cmdlet은 클라우드 서비스에 대 한 AD (Active Directory) 도메인 확장을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-112">The **Set-AzureServiceADDomainExtension** cmdlet enables an AD (Active Directory) Domain extension for a cloud service.</span></span>

## <span data-ttu-id="4876f-113">예제의</span><span class="sxs-lookup"><span data-stu-id="4876f-113">EXAMPLES</span></span>

### <span data-ttu-id="4876f-114">raid-1</span><span class="sxs-lookup"><span data-stu-id="4876f-114">1:</span></span>
```

```

## <span data-ttu-id="4876f-115">변수</span><span class="sxs-lookup"><span data-stu-id="4876f-115">PARAMETERS</span></span>

### <span data-ttu-id="4876f-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="4876f-116">-CertificateThumbprint</span></span>
<span data-ttu-id="4876f-117">개인 구성을 암호화 하는 데 사용할 인증서 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="4876f-118">이 인증서는 인증서 저장소에 이미 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="4876f-119">인증서를 지정 하지 않으면이 cmdlet은 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4876f-120">-Credential</span><span class="sxs-lookup"><span data-stu-id="4876f-120">-Credential</span></span>
<span data-ttu-id="4876f-121">AD 도메인에 가입할 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-121">Specifies the credentials to join the AD domain.</span></span>
<span data-ttu-id="4876f-122">자격 증명에는 사용자 이름 및 암호가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-122">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4876f-123">-DomainName</span><span class="sxs-lookup"><span data-stu-id="4876f-123">-DomainName</span></span>
<span data-ttu-id="4876f-124">광고 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-124">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4876f-125">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="4876f-125">-ExtensionId</span></span>
<span data-ttu-id="4876f-126">확장명 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-126">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4876f-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4876f-127">-InformationAction</span></span>
<span data-ttu-id="4876f-128">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4876f-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4876f-130">하기로</span><span class="sxs-lookup"><span data-stu-id="4876f-130">Continue</span></span>
- <span data-ttu-id="4876f-131">숨기기</span><span class="sxs-lookup"><span data-stu-id="4876f-131">Ignore</span></span>
- <span data-ttu-id="4876f-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="4876f-132">Inquire</span></span>
- <span data-ttu-id="4876f-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4876f-133">SilentlyContinue</span></span>
- <span data-ttu-id="4876f-134">중지가</span><span class="sxs-lookup"><span data-stu-id="4876f-134">Stop</span></span>
- <span data-ttu-id="4876f-135">대기</span><span class="sxs-lookup"><span data-stu-id="4876f-135">Suspend</span></span>

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

### <span data-ttu-id="4876f-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4876f-136">-InformationVariable</span></span>
<span data-ttu-id="4876f-137">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4876f-138">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="4876f-138">-JoinOption</span></span>
<span data-ttu-id="4876f-139">조인 옵션 열거를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-139">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4876f-140">-옵션</span><span class="sxs-lookup"><span data-stu-id="4876f-140">-Options</span></span>
<span data-ttu-id="4876f-141">서명 되지 않은 정수 조인 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-141">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4876f-142">-OUPath</span><span class="sxs-lookup"><span data-stu-id="4876f-142">-OUPath</span></span>
<span data-ttu-id="4876f-143">AD 도메인 가입 작업의 OU (조직 구성 단위) 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-143">Specifies the Organization Unit (OU) path for the AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4876f-144">-프로필</span><span class="sxs-lookup"><span data-stu-id="4876f-144">-Profile</span></span>
<span data-ttu-id="4876f-145">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4876f-146">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4876f-147">-다시 시작</span><span class="sxs-lookup"><span data-stu-id="4876f-147">-Restart</span></span>
<span data-ttu-id="4876f-148">참가 작업이 성공할 경우 컴퓨터를 다시 시작할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-148">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4876f-149">-역할</span><span class="sxs-lookup"><span data-stu-id="4876f-149">-Role</span></span>
<span data-ttu-id="4876f-150">원격 데스크톱 구성을 지정할 역할의 선택적 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-150">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="4876f-151">지정 하지 않으면 AD 도메인 구성이 모든 역할에 대 한 기본 구성으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-151">If not specified the AD domain configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4876f-152">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4876f-152">-ServiceName</span></span>
<span data-ttu-id="4876f-153">클라우드 서비스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-153">Specifies the cloud service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4876f-154">-슬롯</span><span class="sxs-lookup"><span data-stu-id="4876f-154">-Slot</span></span>
<span data-ttu-id="4876f-155">수정할 배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-155">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="4876f-156">이 매개 변수에 허용 되는 값은 프로덕션 또는 스테이징입니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-156">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4876f-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="4876f-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="4876f-158">지문과 함께 인증서를 식별 하는 데 사용 되는 손도장 해시 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-158">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="4876f-159">이 매개 변수는 선택 사항이 며 기본값은 sha1입니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-159">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4876f-160">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="4876f-160">-UnjoinDomainCredential</span></span>
<span data-ttu-id="4876f-161">광고 도메인을 가입을 투 하는 자격 증명 (사용자 이름 및 암호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-161">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4876f-162">-버전</span><span class="sxs-lookup"><span data-stu-id="4876f-162">-Version</span></span>
<span data-ttu-id="4876f-163">확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-163">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4876f-164">-근무 그룹</span><span class="sxs-lookup"><span data-stu-id="4876f-164">-WorkgroupName</span></span>
<span data-ttu-id="4876f-165">작업 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-165">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4876f-166">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="4876f-166">-X509Certificate</span></span>
<span data-ttu-id="4876f-167">지정 된 경우 클라우드 서비스에 자동으로 업로드 되 고 확장 개인 구성을 암호화 하는 데 사용 되는 x509 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-167">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4876f-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4876f-168">CommonParameters</span></span>
<span data-ttu-id="4876f-169">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4876f-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4876f-170">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4876f-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4876f-171">입력</span><span class="sxs-lookup"><span data-stu-id="4876f-171">INPUTS</span></span>

## <span data-ttu-id="4876f-172">출력</span><span class="sxs-lookup"><span data-stu-id="4876f-172">OUTPUTS</span></span>

## <span data-ttu-id="4876f-173">상속자</span><span class="sxs-lookup"><span data-stu-id="4876f-173">NOTES</span></span>

## <span data-ttu-id="4876f-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4876f-174">RELATED LINKS</span></span>

[<span data-ttu-id="4876f-175">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="4876f-175">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="4876f-176">제거-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="4876f-176">Remove-AzureServiceADDomainExtension</span></span>](./Remove-AzureServiceADDomainExtension.md)

[<span data-ttu-id="4876f-177">새-AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="4876f-177">New-AzureServiceADDomainExtensionConfig</span></span>](./New-AzureServiceADDomainExtensionConfig.md)


