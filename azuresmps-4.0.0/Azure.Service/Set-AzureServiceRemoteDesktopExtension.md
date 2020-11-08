---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5C8B1482-80B0-4060-A35D-E9D394156886
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a6303e685ea02408772a237c6b5f154764107e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045813"
---
# <span data-ttu-id="3fbb4-101">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="3fbb4-101">Set-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="3fbb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fbb4-102">SYNOPSIS</span></span>
<span data-ttu-id="3fbb4-103">지정 된 역할 또는 배포 된 서비스에 대 한 모든 역할에 원격 데스크톱 확장을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-103">Enables remote desktop extension on specified role(s) or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="3fbb4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3fbb4-104">SYNTAX</span></span>

### <span data-ttu-id="3fbb4-105">SetExtension (기본값)</span><span class="sxs-lookup"><span data-stu-id="3fbb4-105">SetExtension (Default)</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3fbb4-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="3fbb4-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3fbb4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3fbb4-107">DESCRIPTION</span></span>
<span data-ttu-id="3fbb4-108">**Set-AzureServiceRemoteDesktopExtension** cmdlet을 사용 하면 지정 된 역할 또는 배포 된 서비스의 모든 역할에서 원격 데스크톱 확장을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-108">The **Set-AzureServiceRemoteDesktopExtension** cmdlet enables remote desktop extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="3fbb4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3fbb4-109">EXAMPLES</span></span>

### <span data-ttu-id="3fbb4-110">예제 1: 원격 데스크톱 확장 사용</span><span class="sxs-lookup"><span data-stu-id="3fbb4-110">Example 1: Enable remote desktop extension</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds
```

<span data-ttu-id="3fbb4-111">이 명령은 지정 된 서비스에 대 한 원격 데스크톱 확장을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-111">This command enables the remote desktop extension for the specified service.</span></span>

### <span data-ttu-id="3fbb4-112">예제 2: 지정 된 역할에 대해 원격 데스크톱 확장 사용</span><span class="sxs-lookup"><span data-stu-id="3fbb4-112">Example 2: Enable remote desktop extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds -Role "WebRole1"
```

<span data-ttu-id="3fbb4-113">이 명령은 지정 된 서비스 및 역할에 대 한 원격 데스크톱 확장을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-113">This command enables the remote desktop extension for the specified service and role.</span></span>

## <span data-ttu-id="3fbb4-114">변수</span><span class="sxs-lookup"><span data-stu-id="3fbb4-114">PARAMETERS</span></span>

### <span data-ttu-id="3fbb4-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="3fbb4-115">-CertificateThumbprint</span></span>
<span data-ttu-id="3fbb4-116">개인 구성을 암호화 하는 데 사용할 인증서 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="3fbb4-117">이 인증서는 인증서 저장소에 이미 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="3fbb4-118">인증서를 지정 하지 않으면이 cmdlet은 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="3fbb4-119">-Credential</span><span class="sxs-lookup"><span data-stu-id="3fbb4-119">-Credential</span></span>
<span data-ttu-id="3fbb4-120">원격 데스크톱에 대해 사용 하도록 설정할 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="3fbb4-121">자격 증명에는 사용자 이름 및 암호가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbb4-122">-만료</span><span class="sxs-lookup"><span data-stu-id="3fbb4-122">-Expiration</span></span>
<span data-ttu-id="3fbb4-123">사용자가 만료 될 때 사용자가 지정할 수 있는 날짜 시간 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-123">Specifies a date time object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbb4-124">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="3fbb4-124">-ExtensionId</span></span>
<span data-ttu-id="3fbb4-125">확장명 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbb4-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3fbb4-126">-InformationAction</span></span>
<span data-ttu-id="3fbb4-127">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3fbb4-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3fbb4-129">하기로</span><span class="sxs-lookup"><span data-stu-id="3fbb4-129">Continue</span></span>
- <span data-ttu-id="3fbb4-130">숨기기</span><span class="sxs-lookup"><span data-stu-id="3fbb4-130">Ignore</span></span>
- <span data-ttu-id="3fbb4-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="3fbb4-131">Inquire</span></span>
- <span data-ttu-id="3fbb4-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3fbb4-132">SilentlyContinue</span></span>
- <span data-ttu-id="3fbb4-133">중지가</span><span class="sxs-lookup"><span data-stu-id="3fbb4-133">Stop</span></span>
- <span data-ttu-id="3fbb4-134">대기</span><span class="sxs-lookup"><span data-stu-id="3fbb4-134">Suspend</span></span>

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

### <span data-ttu-id="3fbb4-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3fbb4-135">-InformationVariable</span></span>
<span data-ttu-id="3fbb4-136">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3fbb4-137">-프로필</span><span class="sxs-lookup"><span data-stu-id="3fbb4-137">-Profile</span></span>
<span data-ttu-id="3fbb4-138">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3fbb4-139">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3fbb4-140">-역할</span><span class="sxs-lookup"><span data-stu-id="3fbb4-140">-Role</span></span>
<span data-ttu-id="3fbb4-141">원격 데스크톱 구성을 지정할 역할의 선택적 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="3fbb4-142">이 매개 변수를 지정 하지 않으면 원격 데스크톱 구성이 모든 역할에 대 한 기본 구성으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-142">If this parameter is not specified, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="3fbb4-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3fbb4-143">-ServiceName</span></span>
<span data-ttu-id="3fbb4-144">배포의 Azure 서비스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-144">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="3fbb4-145">-슬롯</span><span class="sxs-lookup"><span data-stu-id="3fbb4-145">-Slot</span></span>
<span data-ttu-id="3fbb4-146">수정할 배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-146">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="3fbb4-147">이 매개 변수에 허용 되는 값은 프로덕션, 스테이징입니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-147">The acceptable values for this parameter are: Production, Staging.</span></span>

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

### <span data-ttu-id="3fbb4-148">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="3fbb4-148">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="3fbb4-149">지문과 함께 인증서를 식별 하는 데 사용 되는 손도장 해시 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-149">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="3fbb4-150">이 매개 변수는 선택 사항이 며 기본값은 sha1입니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-150">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="3fbb4-151">-버전</span><span class="sxs-lookup"><span data-stu-id="3fbb4-151">-Version</span></span>
<span data-ttu-id="3fbb4-152">확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-152">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbb4-153">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="3fbb4-153">-X509Certificate</span></span>
<span data-ttu-id="3fbb4-154">클라우드 서비스에 자동으로 업로드 되 고 확장의 개인 구성을 암호화 하는 데 사용 되는 x509 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-154">Specifies an x509 certificate that is automatically uploaded to the cloud service and used for encrypting the private configuration of the extension.</span></span>

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

### <span data-ttu-id="3fbb4-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fbb4-155">CommonParameters</span></span>
<span data-ttu-id="3fbb4-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fbb4-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fbb4-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fbb4-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fbb4-158">입력</span><span class="sxs-lookup"><span data-stu-id="3fbb4-158">INPUTS</span></span>

## <span data-ttu-id="3fbb4-159">출력</span><span class="sxs-lookup"><span data-stu-id="3fbb4-159">OUTPUTS</span></span>

## <span data-ttu-id="3fbb4-160">상속자</span><span class="sxs-lookup"><span data-stu-id="3fbb4-160">NOTES</span></span>

## <span data-ttu-id="3fbb4-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3fbb4-161">RELATED LINKS</span></span>

[<span data-ttu-id="3fbb4-162">Get-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="3fbb4-162">Get-AzureServiceRemoteDesktopExtension</span></span>](./Get-AzureServiceRemoteDesktopExtension.md)


