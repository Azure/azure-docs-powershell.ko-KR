---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2563898E-C4A0-4530-AB46-30A6FC1BE55C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d295e2198cdbd8168d76b1f8e19e75fb4a662116
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045895"
---
# <span data-ttu-id="ec3d0-101">New-AzureServiceRemoteDesktopExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="ec3d0-101">New-AzureServiceRemoteDesktopExtensionConfig</span></span>

## <span data-ttu-id="ec3d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec3d0-102">SYNOPSIS</span></span>
<span data-ttu-id="ec3d0-103">배포에 대 한 원격 데스크톱 확장 구성을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-103">Generates a remote desktop extension configuration for a deployment.</span></span>

## <span data-ttu-id="ec3d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec3d0-104">SYNTAX</span></span>

### <span data-ttu-id="ec3d0-105">NewExtension (기본값)</span><span class="sxs-lookup"><span data-stu-id="ec3d0-105">NewExtension (Default)</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ec3d0-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="ec3d0-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ec3d0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ec3d0-107">DESCRIPTION</span></span>
<span data-ttu-id="ec3d0-108">**새로운-AzureServiceRemoteDesktopExtensionConfig** cmdlet은 배포용 원격 데스크톱 확장에 대 한 구성을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-108">The **New-AzureServiceRemoteDesktopExtensionConfig** cmdlet generates a configuration for a remote desktop extension for a deployment.</span></span>

## <span data-ttu-id="ec3d0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ec3d0-109">EXAMPLES</span></span>

### <span data-ttu-id="ec3d0-110">예제 1: 원격 데스크톱 확장 구성 생성</span><span class="sxs-lookup"><span data-stu-id="ec3d0-110">Example 1: Generate a remote desktop extension configuration</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred
```

<span data-ttu-id="ec3d0-111">이 명령은 지정 된 자격 증명에 대 한 원격 데스크톱 확장 구성을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-111">This command generates a remote desktop extension configuration for the specified credentials.</span></span>

### <span data-ttu-id="ec3d0-112">예제 2: 지정 된 역할에 대 한 원격 데스크톱 확장 구성 생성</span><span class="sxs-lookup"><span data-stu-id="ec3d0-112">Example 2: Generate a remote desktop extension configuration for a specified role</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred -Role "WebRole01"
```

<span data-ttu-id="ec3d0-113">이 명령은 지정 된 자격 증명과 WebRole01 역할에 대 한 원격 데스크톱 확장 구성을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-113">This command generates a remote desktop extension configuration for the specified credentials and the WebRole01 role.</span></span>

## <span data-ttu-id="ec3d0-114">변수</span><span class="sxs-lookup"><span data-stu-id="ec3d0-114">PARAMETERS</span></span>

### <span data-ttu-id="ec3d0-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ec3d0-115">-CertificateThumbprint</span></span>
<span data-ttu-id="ec3d0-116">개인 구성을 암호화 하는 데 사용할 인증서 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="ec3d0-117">이 인증서는 인증서 저장소에 이미 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="ec3d0-118">인증서를 지정 하지 않으면이 cmdlet은 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="ec3d0-119">-Credential</span><span class="sxs-lookup"><span data-stu-id="ec3d0-119">-Credential</span></span>
<span data-ttu-id="ec3d0-120">원격 데스크톱에 대해 사용 하도록 설정할 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="ec3d0-121">자격 증명에는 사용자 이름 및 암호가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec3d0-122">-만료</span><span class="sxs-lookup"><span data-stu-id="ec3d0-122">-Expiration</span></span>
<span data-ttu-id="ec3d0-123">사용자가 만료 되는 시간을 사용자가 지정할 수 있도록 하는 **DateTime** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-123">Specifies a **DateTime** object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec3d0-124">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="ec3d0-124">-ExtensionId</span></span>
<span data-ttu-id="ec3d0-125">확장명 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec3d0-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ec3d0-126">-InformationAction</span></span>
<span data-ttu-id="ec3d0-127">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ec3d0-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ec3d0-129">하기로</span><span class="sxs-lookup"><span data-stu-id="ec3d0-129">Continue</span></span>
- <span data-ttu-id="ec3d0-130">숨기기</span><span class="sxs-lookup"><span data-stu-id="ec3d0-130">Ignore</span></span>
- <span data-ttu-id="ec3d0-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="ec3d0-131">Inquire</span></span>
- <span data-ttu-id="ec3d0-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ec3d0-132">SilentlyContinue</span></span>
- <span data-ttu-id="ec3d0-133">중지가</span><span class="sxs-lookup"><span data-stu-id="ec3d0-133">Stop</span></span>
- <span data-ttu-id="ec3d0-134">대기</span><span class="sxs-lookup"><span data-stu-id="ec3d0-134">Suspend</span></span>

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

### <span data-ttu-id="ec3d0-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ec3d0-135">-InformationVariable</span></span>
<span data-ttu-id="ec3d0-136">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ec3d0-137">-프로필</span><span class="sxs-lookup"><span data-stu-id="ec3d0-137">-Profile</span></span>
<span data-ttu-id="ec3d0-138">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ec3d0-139">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ec3d0-140">-역할</span><span class="sxs-lookup"><span data-stu-id="ec3d0-140">-Role</span></span>
<span data-ttu-id="ec3d0-141">원격 데스크톱 구성을 지정할 역할의 선택적 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="ec3d0-142">이 매개 변수를 지정 하지 않으면 원격 데스크톱 구성이 모든 역할에 대 한 기본 구성으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-142">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="ec3d0-143">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="ec3d0-143">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="ec3d0-144">지문과 함께 인증서를 식별 하는 데 사용 되는 손도장 해시 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-144">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="ec3d0-145">이 매개 변수는 선택 사항이 며 기본값은 sha1입니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-145">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="ec3d0-146">-버전</span><span class="sxs-lookup"><span data-stu-id="ec3d0-146">-Version</span></span>
<span data-ttu-id="ec3d0-147">확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-147">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec3d0-148">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="ec3d0-148">-X509Certificate</span></span>
<span data-ttu-id="ec3d0-149">지정 된 경우 클라우드 서비스에 자동으로 업로드 되 고 확장 개인 구성을 암호화 하는 데 사용 되는 x509 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-149">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="ec3d0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec3d0-150">CommonParameters</span></span>
<span data-ttu-id="ec3d0-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec3d0-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec3d0-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec3d0-153">입력</span><span class="sxs-lookup"><span data-stu-id="ec3d0-153">INPUTS</span></span>

## <span data-ttu-id="ec3d0-154">출력</span><span class="sxs-lookup"><span data-stu-id="ec3d0-154">OUTPUTS</span></span>

## <span data-ttu-id="ec3d0-155">상속자</span><span class="sxs-lookup"><span data-stu-id="ec3d0-155">NOTES</span></span>

## <span data-ttu-id="ec3d0-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec3d0-156">RELATED LINKS</span></span>

[<span data-ttu-id="ec3d0-157">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="ec3d0-157">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


