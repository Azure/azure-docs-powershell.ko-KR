---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D37920D3-AF6C-4CFC-B9A3-8ED931AEC0DC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 318683c26d05c624549363ff1afe4a2b963c1fe6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045447"
---
# <span data-ttu-id="c4af8-101">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="c4af8-101">Set-AzureServiceExtension</span></span>

## <span data-ttu-id="c4af8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4af8-102">SYNOPSIS</span></span>
<span data-ttu-id="c4af8-103">클라우드 서비스 확장을 배포에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-103">Adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="c4af8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c4af8-104">SYNTAX</span></span>

### <span data-ttu-id="c4af8-105">SetExtension (기본값)</span><span class="sxs-lookup"><span data-stu-id="c4af8-105">SetExtension (Default)</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c4af8-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="c4af8-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c4af8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c4af8-107">DESCRIPTION</span></span>
<span data-ttu-id="c4af8-108">**Set-AzureServiceExtension** cmdlet은 배포에 클라우드 서비스 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-108">The **Set-AzureServiceExtension** cmdlet adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="c4af8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c4af8-109">EXAMPLES</span></span>

### <span data-ttu-id="c4af8-110">예제 1: 배포에 클라우드 서비스 추가</span><span class="sxs-lookup"><span data-stu-id="c4af8-110">Example 1: Add a cloud service to a deployment</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -ExtensionName "RDP" -Version "1.0" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="c4af8-111">이 명령은 클라우드 서비스를 배포에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-111">This command adds a cloud service to a deployment.</span></span>

### <span data-ttu-id="c4af8-112">예제 2: 지정 된 역할에 대 한 배포에 클라우드 서비스 추가</span><span class="sxs-lookup"><span data-stu-id="c4af8-112">Example 2: Add a cloud service to a deployment for a specified role</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -Role "WebRole1" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="c4af8-113">이 명령은 지정 된 역할에 대 한 배포에 클라우드 서비스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-113">This command adds a cloud service to a deployment for a specified role.</span></span>

## <span data-ttu-id="c4af8-114">변수</span><span class="sxs-lookup"><span data-stu-id="c4af8-114">PARAMETERS</span></span>

### <span data-ttu-id="c4af8-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="c4af8-115">-CertificateThumbprint</span></span>
<span data-ttu-id="c4af8-116">개인 구성을 암호화 하는 데 사용할 인증서 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="c4af8-117">이 인증서는 인증서 저장소에 이미 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="c4af8-118">인증서를 지정 하지 않으면이 cmdlet은 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4af8-119">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="c4af8-119">-ExtensionId</span></span>
<span data-ttu-id="c4af8-120">확장명 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-120">Specifies the extension ID.</span></span>

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

### <span data-ttu-id="c4af8-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="c4af8-121">-ExtensionName</span></span>
<span data-ttu-id="c4af8-122">확장명 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-122">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4af8-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c4af8-123">-InformationAction</span></span>
<span data-ttu-id="c4af8-124">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c4af8-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c4af8-126">하기로</span><span class="sxs-lookup"><span data-stu-id="c4af8-126">Continue</span></span>
- <span data-ttu-id="c4af8-127">숨기기</span><span class="sxs-lookup"><span data-stu-id="c4af8-127">Ignore</span></span>
- <span data-ttu-id="c4af8-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="c4af8-128">Inquire</span></span>
- <span data-ttu-id="c4af8-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c4af8-129">SilentlyContinue</span></span>
- <span data-ttu-id="c4af8-130">중지가</span><span class="sxs-lookup"><span data-stu-id="c4af8-130">Stop</span></span>
- <span data-ttu-id="c4af8-131">대기</span><span class="sxs-lookup"><span data-stu-id="c4af8-131">Suspend</span></span>

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

### <span data-ttu-id="c4af8-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c4af8-132">-InformationVariable</span></span>
<span data-ttu-id="c4af8-133">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c4af8-134">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4af8-134">-PrivateConfiguration</span></span>
<span data-ttu-id="c4af8-135">개인 구성 텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-135">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4af8-136">-프로필</span><span class="sxs-lookup"><span data-stu-id="c4af8-136">-Profile</span></span>
<span data-ttu-id="c4af8-137">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c4af8-138">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c4af8-139">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="c4af8-139">-ProviderNamespace</span></span>
<span data-ttu-id="c4af8-140">확장 공급자 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-140">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4af8-141">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4af8-141">-PublicConfiguration</span></span>
<span data-ttu-id="c4af8-142">공용 구성 텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-142">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4af8-143">-역할</span><span class="sxs-lookup"><span data-stu-id="c4af8-143">-Role</span></span>
<span data-ttu-id="c4af8-144">원격 데스크톱 구성을 지정할 역할의 선택적 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-144">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="c4af8-145">이 매개 변수를 지정 하지 않으면 원격 데스크톱 구성이 모든 역할에 대 한 기본 구성으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-145">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="c4af8-146">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c4af8-146">-ServiceName</span></span>
<span data-ttu-id="c4af8-147">배포의 Azure 서비스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-147">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="c4af8-148">-슬롯</span><span class="sxs-lookup"><span data-stu-id="c4af8-148">-Slot</span></span>
<span data-ttu-id="c4af8-149">수정할 배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-149">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="c4af8-150">유효한 값은 프로덕션 또는 스테이징입니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-150">Valid values are: Production or Staging.</span></span>

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

### <span data-ttu-id="c4af8-151">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="c4af8-151">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="c4af8-152">지문과 함께 인증서를 식별 하는 데 사용 되는 손도장 해시 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-152">Specifies the thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="c4af8-153">이 매개 변수는 선택 사항이 며 기본값은 sha1입니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-153">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="c4af8-154">-버전</span><span class="sxs-lookup"><span data-stu-id="c4af8-154">-Version</span></span>
<span data-ttu-id="c4af8-155">확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-155">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4af8-156">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="c4af8-156">-X509Certificate</span></span>
<span data-ttu-id="c4af8-157">클라우드 서비스에 자동으로 업로드 되 고 확장 개인 구성을 암호화 하는 데 사용 되는 x.509 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-157">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: SetExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4af8-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4af8-158">CommonParameters</span></span>
<span data-ttu-id="c4af8-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4af8-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4af8-160">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4af8-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4af8-161">입력</span><span class="sxs-lookup"><span data-stu-id="c4af8-161">INPUTS</span></span>

## <span data-ttu-id="c4af8-162">출력</span><span class="sxs-lookup"><span data-stu-id="c4af8-162">OUTPUTS</span></span>

## <span data-ttu-id="c4af8-163">상속자</span><span class="sxs-lookup"><span data-stu-id="c4af8-163">NOTES</span></span>

## <span data-ttu-id="c4af8-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4af8-164">RELATED LINKS</span></span>

[<span data-ttu-id="c4af8-165">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="c4af8-165">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="c4af8-166">-AzureServiceExtension 제거</span><span class="sxs-lookup"><span data-stu-id="c4af8-166">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)


