---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DFD4BA63-A7DE-49DD-878C-68062EF17873
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d4830d049ab01142c75847b4afd5419729f14d1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045897"
---
# <span data-ttu-id="5ae4a-101">New-AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="5ae4a-101">New-AzureServiceADDomainExtensionConfig</span></span>

## <span data-ttu-id="5ae4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ae4a-102">SYNOPSIS</span></span>
<span data-ttu-id="5ae4a-103">클라우드 서비스의 AD 도메인 확장에 대 한 구성을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-103">Generates the configuration for the AD domain extension for cloud services.</span></span>

## <span data-ttu-id="5ae4a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5ae4a-104">SYNTAX</span></span>

### <span data-ttu-id="5ae4a-105">JoinDomainUsingEnumOptions (기본값)</span><span class="sxs-lookup"><span data-stu-id="5ae4a-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5ae4a-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="5ae4a-106">JoinDomainUsingJoinOption</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5ae4a-107">근무 그룹</span><span class="sxs-lookup"><span data-stu-id="5ae4a-107">WorkGroupName</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5ae4a-108">JoinDomainUsingEnumOptionsAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="5ae4a-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5ae4a-109">JoinDomainUsingJoinOptionAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="5ae4a-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5ae4a-110">WorkGroupNameThumbprint</span><span class="sxs-lookup"><span data-stu-id="5ae4a-110">WorkGroupNameThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5ae4a-111">설명은</span><span class="sxs-lookup"><span data-stu-id="5ae4a-111">DESCRIPTION</span></span>
<span data-ttu-id="5ae4a-112">**새-AzureServiceADDomainExtensionConfig** cmdlet은 클라우드 서비스의 AD (Active Directory) 도메인 확장에 대 한 구성을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-112">The **New-AzureServiceADDomainExtensionConfig** cmdlet generates the configuration for the Active Directory (AD) domain extension for cloud services.</span></span>

## <span data-ttu-id="5ae4a-113">예제의</span><span class="sxs-lookup"><span data-stu-id="5ae4a-113">EXAMPLES</span></span>

### <span data-ttu-id="5ae4a-114">예제 1: AD 도메인 구성 지정</span><span class="sxs-lookup"><span data-stu-id="5ae4a-114">Example 1: Specify an AD domain configuration</span></span>
```
PS C:\> $ExtensionCfg = New-AzureServiceADDomainExtensionConfig -Role WorkerRole1 -DomainName $Domain -Credential $Cred -JoinOption 35;

PS C:\> New-AzureDeployment -ServiceName $CloudSvc -Slot "Production" -Package $Pkg -Configuration $Config -ExtensionConfiguration $ExtensionCfg;
```

<span data-ttu-id="5ae4a-115">이 명령은 AD 도메인 확장에 대 한 구성을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-115">This command generates a configuration for the AD domain extension.</span></span>

## <span data-ttu-id="5ae4a-116">변수</span><span class="sxs-lookup"><span data-stu-id="5ae4a-116">PARAMETERS</span></span>

### <span data-ttu-id="5ae4a-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="5ae4a-117">-CertificateThumbprint</span></span>
<span data-ttu-id="5ae4a-118">개인 구성을 암호화 하는 데 사용할 인증서 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-118">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="5ae4a-119">이 인증서는 인증서 저장소에 이미 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-119">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="5ae4a-120">인증서를 지정 하지 않으면이 cmdlet은 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-120">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae4a-121">-Credential</span><span class="sxs-lookup"><span data-stu-id="5ae4a-121">-Credential</span></span>
<span data-ttu-id="5ae4a-122">광고 도메인에 참가 하는 데 사용할 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-122">Specifies the credentials to use to join the AD domain.</span></span>
<span data-ttu-id="5ae4a-123">자격 증명에는 사용자 이름 및 암호가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-123">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae4a-124">-DomainName</span><span class="sxs-lookup"><span data-stu-id="5ae4a-124">-DomainName</span></span>
<span data-ttu-id="5ae4a-125">광고 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-125">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae4a-126">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="5ae4a-126">-ExtensionId</span></span>
<span data-ttu-id="5ae4a-127">확장명 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-127">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae4a-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5ae4a-128">-InformationAction</span></span>
<span data-ttu-id="5ae4a-129">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5ae4a-130">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5ae4a-131">하기로</span><span class="sxs-lookup"><span data-stu-id="5ae4a-131">Continue</span></span>
- <span data-ttu-id="5ae4a-132">숨기기</span><span class="sxs-lookup"><span data-stu-id="5ae4a-132">Ignore</span></span>
- <span data-ttu-id="5ae4a-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="5ae4a-133">Inquire</span></span>
- <span data-ttu-id="5ae4a-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5ae4a-134">SilentlyContinue</span></span>
- <span data-ttu-id="5ae4a-135">중지가</span><span class="sxs-lookup"><span data-stu-id="5ae4a-135">Stop</span></span>
- <span data-ttu-id="5ae4a-136">대기</span><span class="sxs-lookup"><span data-stu-id="5ae4a-136">Suspend</span></span>

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

### <span data-ttu-id="5ae4a-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5ae4a-137">-InformationVariable</span></span>
<span data-ttu-id="5ae4a-138">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5ae4a-139">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="5ae4a-139">-JoinOption</span></span>
<span data-ttu-id="5ae4a-140">조인 옵션 열거를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-140">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae4a-141">-옵션</span><span class="sxs-lookup"><span data-stu-id="5ae4a-141">-Options</span></span>
<span data-ttu-id="5ae4a-142">서명 되지 않은 정수 조인 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-142">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae4a-143">-OUPath</span><span class="sxs-lookup"><span data-stu-id="5ae4a-143">-OUPath</span></span>
<span data-ttu-id="5ae4a-144">AD 도메인 가입 작업에 대 한 OU (조직 구성 단위) 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-144">Specifies the organization unit (OU) path for AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae4a-145">-프로필</span><span class="sxs-lookup"><span data-stu-id="5ae4a-145">-Profile</span></span>
<span data-ttu-id="5ae4a-146">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5ae4a-147">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5ae4a-148">-다시 시작</span><span class="sxs-lookup"><span data-stu-id="5ae4a-148">-Restart</span></span>
<span data-ttu-id="5ae4a-149">참가 작업이 성공할 경우 컴퓨터를 다시 시작할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-149">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae4a-150">-역할</span><span class="sxs-lookup"><span data-stu-id="5ae4a-150">-Role</span></span>
<span data-ttu-id="5ae4a-151">AD 도메인 구성에 대 한 원격 데스크톱 구성을 지정할 역할의 선택적 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-151">Specifies an optional array of roles to specify the remote desktop configuration for the AD domain configuration.</span></span>
<span data-ttu-id="5ae4a-152">이 매개 변수를 지정 하지 않으면 AD 도메인 구성이 모든 역할에 대 한 기본 구성으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-152">If you do not specify this parameter, the AD domain configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae4a-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="5ae4a-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="5ae4a-154">지문과 함께 인증서를 식별 하는 데 사용 되는 손도장 해시 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-154">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="5ae4a-155">이 매개 변수는 선택 사항이 며 기본값은 sha1입니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-155">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae4a-156">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="5ae4a-156">-UnjoinDomainCredential</span></span>
<span data-ttu-id="5ae4a-157">광고 도메인을 가입을 투 하는 자격 증명 (사용자 이름 및 암호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-157">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae4a-158">-버전</span><span class="sxs-lookup"><span data-stu-id="5ae4a-158">-Version</span></span>
<span data-ttu-id="5ae4a-159">확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-159">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae4a-160">-근무 그룹</span><span class="sxs-lookup"><span data-stu-id="5ae4a-160">-WorkgroupName</span></span>
<span data-ttu-id="5ae4a-161">작업 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-161">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae4a-162">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="5ae4a-162">-X509Certificate</span></span>
<span data-ttu-id="5ae4a-163">클라우드 서비스에 자동으로 업로드 되 고 확장 개인 구성을 암호화 하는 데 사용 되는 x.509 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-163">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae4a-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ae4a-164">CommonParameters</span></span>
<span data-ttu-id="5ae4a-165">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ae4a-166">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ae4a-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ae4a-167">입력</span><span class="sxs-lookup"><span data-stu-id="5ae4a-167">INPUTS</span></span>

## <span data-ttu-id="5ae4a-168">출력</span><span class="sxs-lookup"><span data-stu-id="5ae4a-168">OUTPUTS</span></span>

## <span data-ttu-id="5ae4a-169">상속자</span><span class="sxs-lookup"><span data-stu-id="5ae4a-169">NOTES</span></span>

## <span data-ttu-id="5ae4a-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ae4a-170">RELATED LINKS</span></span>

[<span data-ttu-id="5ae4a-171">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5ae4a-171">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="5ae4a-172">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5ae4a-172">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


