---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1F76C63E-5289-4F88-9522-3FF4EF732908
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a232ec03da38ea3d527dcd9aa214dbf681bcc6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045898"
---
# <span data-ttu-id="ae1cc-101">New-AzureServiceDiagnosticsExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="ae1cc-101">New-AzureServiceDiagnosticsExtensionConfig</span></span>

## <span data-ttu-id="ae1cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae1cc-102">SYNOPSIS</span></span>
<span data-ttu-id="ae1cc-103">지정 된 역할 또는 모든 역할에 대 한 진단 확장 구성을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-103">Generates a configuration for a diagnostics extension for specified role(s) or all roles.</span></span>

## <span data-ttu-id="ae1cc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae1cc-104">SYNTAX</span></span>

### <span data-ttu-id="ae1cc-105">NewExtension (기본값)</span><span class="sxs-lookup"><span data-stu-id="ae1cc-105">NewExtension (Default)</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ae1cc-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="ae1cc-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>]
 [[-StorageContext] <AzureStorageContext>] [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae1cc-107">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="ae1cc-107">SetExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ae1cc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ae1cc-108">DESCRIPTION</span></span>
<span data-ttu-id="ae1cc-109">**AzureServiceDiagnosticsExtensionConfig** cmdlet은 지정 된 역할 또는 모든 역할에 대 한 진단 확장 구성을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-109">The **New-AzureServiceDiagnosticsExtensionConfig** cmdlet generates a configuration for a diagnostics extension for specified roles or all roles.</span></span>

## <span data-ttu-id="ae1cc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ae1cc-110">EXAMPLES</span></span>

### <span data-ttu-id="ae1cc-111">예제 1: 클라우드 서비스의 모든 역할에 대 한 Azure 진단 확장 만들기</span><span class="sxs-lookup"><span data-stu-id="ae1cc-111">Example 1: Create the Azure Diagnostics extension for all roles in the cloud service</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="ae1cc-112">이 명령은 클라우드 서비스의 모든 역할에 대 한 Azure 진단 확장을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-112">This command creates the Azure Diagnostics extension for all of the roles in the cloud service.</span></span>

### <span data-ttu-id="ae1cc-113">예제 2: 역할에 대 한 Azure 진단 확장 만들기</span><span class="sxs-lookup"><span data-stu-id="ae1cc-113">Example 2: Create the Azure Diagnostics extension for a role</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole1"
```

<span data-ttu-id="ae1cc-114">이 명령은 클라우드 서비스의 역할 WebRole01에 대 한 Azure 진단 확장을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-114">This command creates the Azure Diagnostics extension for the role WebRole01 in the cloud service.</span></span>

## <span data-ttu-id="ae1cc-115">변수</span><span class="sxs-lookup"><span data-stu-id="ae1cc-115">PARAMETERS</span></span>

### <span data-ttu-id="ae1cc-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ae1cc-116">-CertificateThumbprint</span></span>
<span data-ttu-id="ae1cc-117">개인 구성을 암호화 하는 데 사용할 인증서 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="ae1cc-118">이 인증서는 인증서 저장소에 이미 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="ae1cc-119">인증서를 지정 하지 않으면이 cmdlet은 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="ae1cc-120">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="ae1cc-120">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="ae1cc-121">진단 구성 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-121">Specifies the diagnostics configuration path.</span></span>

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

### <span data-ttu-id="ae1cc-122">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="ae1cc-122">-ExtensionId</span></span>
<span data-ttu-id="ae1cc-123">확장명 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-123">Specifies the extension ID.</span></span>

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

### <span data-ttu-id="ae1cc-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ae1cc-124">-InformationAction</span></span>
<span data-ttu-id="ae1cc-125">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ae1cc-126">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae1cc-127">하기로</span><span class="sxs-lookup"><span data-stu-id="ae1cc-127">Continue</span></span>
- <span data-ttu-id="ae1cc-128">숨기기</span><span class="sxs-lookup"><span data-stu-id="ae1cc-128">Ignore</span></span>
- <span data-ttu-id="ae1cc-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="ae1cc-129">Inquire</span></span>
- <span data-ttu-id="ae1cc-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ae1cc-130">SilentlyContinue</span></span>
- <span data-ttu-id="ae1cc-131">중지가</span><span class="sxs-lookup"><span data-stu-id="ae1cc-131">Stop</span></span>
- <span data-ttu-id="ae1cc-132">대기</span><span class="sxs-lookup"><span data-stu-id="ae1cc-132">Suspend</span></span>

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

### <span data-ttu-id="ae1cc-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ae1cc-133">-InformationVariable</span></span>
<span data-ttu-id="ae1cc-134">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ae1cc-135">-프로필</span><span class="sxs-lookup"><span data-stu-id="ae1cc-135">-Profile</span></span>
<span data-ttu-id="ae1cc-136">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ae1cc-137">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ae1cc-138">-역할</span><span class="sxs-lookup"><span data-stu-id="ae1cc-138">-Role</span></span>
<span data-ttu-id="ae1cc-139">진단 구성을 지정할 역할의 선택적 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-139">Specifies an optional array of roles to specify the diagnostics configuration for.</span></span>
<span data-ttu-id="ae1cc-140">지정 하지 않으면 진단 구성이 모든 역할에 대 한 기본 구성으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-140">If not specified the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1cc-141">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="ae1cc-141">-StorageAccountEndpoint</span></span>
<span data-ttu-id="ae1cc-142">저장소 계정 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-142">Specifies the storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1cc-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ae1cc-143">-StorageAccountKey</span></span>
<span data-ttu-id="ae1cc-144">저장소 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-144">Specifies the storage account key.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1cc-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ae1cc-145">-StorageAccountName</span></span>
<span data-ttu-id="ae1cc-146">저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-146">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1cc-147">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="ae1cc-147">-StorageContext</span></span>
<span data-ttu-id="ae1cc-148">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-148">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1cc-149">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="ae1cc-149">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="ae1cc-150">지문과 함께 인증서를 식별 하는 데 사용 되는 손도장 해시 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-150">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="ae1cc-151">이 매개 변수는 선택 사항이 며 기본값은 sha1입니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-151">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="ae1cc-152">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="ae1cc-152">-X509Certificate</span></span>
<span data-ttu-id="ae1cc-153">클라우드 서비스에 자동으로 업로드 되 고 확장 개인 구성을 암호화 하는 데 사용 되는 x.509 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-153">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="ae1cc-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae1cc-154">CommonParameters</span></span>
<span data-ttu-id="ae1cc-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae1cc-156">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae1cc-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae1cc-157">입력</span><span class="sxs-lookup"><span data-stu-id="ae1cc-157">INPUTS</span></span>

## <span data-ttu-id="ae1cc-158">출력</span><span class="sxs-lookup"><span data-stu-id="ae1cc-158">OUTPUTS</span></span>

## <span data-ttu-id="ae1cc-159">상속자</span><span class="sxs-lookup"><span data-stu-id="ae1cc-159">NOTES</span></span>

## <span data-ttu-id="ae1cc-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae1cc-160">RELATED LINKS</span></span>

[<span data-ttu-id="ae1cc-161">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ae1cc-161">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="ae1cc-162">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ae1cc-162">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


