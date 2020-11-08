---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E27283AF-4057-48D9-9F08-7D36290DD907
online version: ''
schema: 2.0.0
ms.openlocfilehash: dfe55fb2ced2275eae06e96480249acd99d3ad6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045896"
---
# <span data-ttu-id="9a50d-101">New-AzureServiceExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="9a50d-101">New-AzureServiceExtensionConfig</span></span>

## <span data-ttu-id="9a50d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a50d-102">SYNOPSIS</span></span>
<span data-ttu-id="9a50d-103">배포에 대 한 클라우드 서비스 확장 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-103">Creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="9a50d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a50d-104">SYNTAX</span></span>

### <span data-ttu-id="9a50d-105">NewExtension (기본값)</span><span class="sxs-lookup"><span data-stu-id="9a50d-105">NewExtension (Default)</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a50d-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="9a50d-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a50d-107">UpdateExtensionStatusParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9a50d-107">UpdateExtensionStatusParameterSetName</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-ExtensionId] <String> [-ExtensionState] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a50d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9a50d-108">DESCRIPTION</span></span>
<span data-ttu-id="9a50d-109">**새-AzureServiceExtensionConfig** cmdlet은 배포에 대 한 클라우드 서비스 확장 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-109">The **New-AzureServiceExtensionConfig** cmdlet creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="9a50d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9a50d-110">EXAMPLES</span></span>

### <span data-ttu-id="9a50d-111">예제 1: 확장 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="9a50d-111">Example 1: Create an extension configuration</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -ExtensionName 'RDP' -Version '1.0' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="9a50d-112">이 명령은 확장 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-112">This command specifies an extension configuration.</span></span>

### <span data-ttu-id="9a50d-113">예제 2: 역할에 대 한 확장 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="9a50d-113">Example 2: Create an extension configuration for a role</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -Role WebRole1 -ExtensionName 'RDP' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="9a50d-114">이 명령은 역할 WebRole1에 대 한 확장 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-114">This command specifies an extension configuration for the role WebRole1.</span></span>

## <span data-ttu-id="9a50d-115">변수</span><span class="sxs-lookup"><span data-stu-id="9a50d-115">PARAMETERS</span></span>

### <span data-ttu-id="9a50d-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="9a50d-116">-CertificateThumbprint</span></span>
<span data-ttu-id="9a50d-117">개인 구성을 암호화 하는 데 사용할 인증서 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="9a50d-118">이 인증서는 인증서 저장소에 이미 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="9a50d-119">인증서를 지정 하지 않으면이 cmdlet은 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a50d-120">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="9a50d-120">-ExtensionId</span></span>
<span data-ttu-id="9a50d-121">확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-121">Specifies the name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a50d-122">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="9a50d-122">-ExtensionName</span></span>
<span data-ttu-id="9a50d-123">확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-123">Specifies the name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a50d-124">-ExtensionState</span><span class="sxs-lookup"><span data-stu-id="9a50d-124">-ExtensionState</span></span>
<span data-ttu-id="9a50d-125">확장의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-125">Specifies the state of the extension.</span></span>
<span data-ttu-id="9a50d-126">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9a50d-127">설정할</span><span class="sxs-lookup"><span data-stu-id="9a50d-127">Enable</span></span> 
- <span data-ttu-id="9a50d-128">설정할</span><span class="sxs-lookup"><span data-stu-id="9a50d-128">Disable</span></span> 
- <span data-ttu-id="9a50d-129">Uninstall</span><span class="sxs-lookup"><span data-stu-id="9a50d-129">Uninstall</span></span>

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a50d-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9a50d-130">-InformationAction</span></span>
<span data-ttu-id="9a50d-131">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9a50d-132">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9a50d-133">하기로</span><span class="sxs-lookup"><span data-stu-id="9a50d-133">Continue</span></span>
- <span data-ttu-id="9a50d-134">숨기기</span><span class="sxs-lookup"><span data-stu-id="9a50d-134">Ignore</span></span>
- <span data-ttu-id="9a50d-135">Inquire</span><span class="sxs-lookup"><span data-stu-id="9a50d-135">Inquire</span></span>
- <span data-ttu-id="9a50d-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9a50d-136">SilentlyContinue</span></span>
- <span data-ttu-id="9a50d-137">중지가</span><span class="sxs-lookup"><span data-stu-id="9a50d-137">Stop</span></span>
- <span data-ttu-id="9a50d-138">대기</span><span class="sxs-lookup"><span data-stu-id="9a50d-138">Suspend</span></span>

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

### <span data-ttu-id="9a50d-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9a50d-139">-InformationVariable</span></span>
<span data-ttu-id="9a50d-140">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9a50d-141">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a50d-141">-PrivateConfiguration</span></span>
<span data-ttu-id="9a50d-142">개인 구성 텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-142">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a50d-143">-프로필</span><span class="sxs-lookup"><span data-stu-id="9a50d-143">-Profile</span></span>
<span data-ttu-id="9a50d-144">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-144">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9a50d-145">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-145">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9a50d-146">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="9a50d-146">-ProviderNamespace</span></span>
<span data-ttu-id="9a50d-147">확장명의 공급자 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-147">Specifies the Extension's Provider Namespace.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a50d-148">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a50d-148">-PublicConfiguration</span></span>
<span data-ttu-id="9a50d-149">공용 구성 텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-149">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a50d-150">-역할</span><span class="sxs-lookup"><span data-stu-id="9a50d-150">-Role</span></span>
<span data-ttu-id="9a50d-151">원격 데스크톱 구성을 지정할 역할의 선택적 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-151">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="9a50d-152">지정 하지 않으면 원격 데스크톱 구성이 모든 역할에 대 한 기본 구성으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-152">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="9a50d-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="9a50d-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="9a50d-154">지문과 함께 인증서를 식별 하는 데 사용 되는 손도장 해시 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-154">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="9a50d-155">이 매개 변수는 선택 사항이 며 기본값은 sha1입니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-155">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a50d-156">-버전</span><span class="sxs-lookup"><span data-stu-id="9a50d-156">-Version</span></span>
<span data-ttu-id="9a50d-157">확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-157">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a50d-158">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="9a50d-158">-X509Certificate</span></span>
<span data-ttu-id="9a50d-159">지정 된 경우 클라우드 서비스에 자동으로 업로드 되 고 확장 개인 구성을 암호화 하는 데 사용 되는 x509 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-159">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: NewExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a50d-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a50d-160">CommonParameters</span></span>
<span data-ttu-id="9a50d-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50d-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a50d-162">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a50d-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a50d-163">입력</span><span class="sxs-lookup"><span data-stu-id="9a50d-163">INPUTS</span></span>

## <span data-ttu-id="9a50d-164">출력</span><span class="sxs-lookup"><span data-stu-id="9a50d-164">OUTPUTS</span></span>

## <span data-ttu-id="9a50d-165">상속자</span><span class="sxs-lookup"><span data-stu-id="9a50d-165">NOTES</span></span>

## <span data-ttu-id="9a50d-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a50d-166">RELATED LINKS</span></span>

[<span data-ttu-id="9a50d-167">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="9a50d-167">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="9a50d-168">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="9a50d-168">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


