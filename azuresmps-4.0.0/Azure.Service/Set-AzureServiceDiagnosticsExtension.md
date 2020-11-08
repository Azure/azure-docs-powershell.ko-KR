---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2E738CEF-BBDD-425D-B12C-86FF7C45A634
online version: ''
schema: 2.0.0
ms.openlocfilehash: 518528d4af8889cf36b30c417e0170e0ea228ebf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046047"
---
# <span data-ttu-id="fad80-101">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fad80-101">Set-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="fad80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fad80-102">SYNOPSIS</span></span>
<span data-ttu-id="fad80-103">지정 된 역할 또는 배포 된 서비스에 대 한 모든 역할에 대해 Azure 진단 확장을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-103">Enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="fad80-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fad80-104">SYNTAX</span></span>

### <span data-ttu-id="fad80-105">SetExtension (기본값)</span><span class="sxs-lookup"><span data-stu-id="fad80-105">SetExtension (Default)</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="fad80-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="fad80-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-CertificateThumbprint] <String>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="fad80-107">SetExtensionUsingDiagnosticsConfiguration</span><span class="sxs-lookup"><span data-stu-id="fad80-107">SetExtensionUsingDiagnosticsConfiguration</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-DiagnosticsConfiguration] <ExtensionConfigurationInput[]> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fad80-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fad80-108">DESCRIPTION</span></span>
<span data-ttu-id="fad80-109">AzureServiceDiagnosticsExtension cmdlet은 지정 된 역할 또는 배포 된 서비스에 대 한 모든 역할에 대해 Azure 진단 확장을 사용 하도록 **설정** 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-109">The **Set-AzureServiceDiagnosticsExtension** cmdlet enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="fad80-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fad80-110">EXAMPLES</span></span>

### <span data-ttu-id="fad80-111">예제 1: Azure 진단 확장 사용</span><span class="sxs-lookup"><span data-stu-id="fad80-111">Example 1: Enable Azure Diagnostics extension</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="fad80-112">이 명령은 모든 역할에 대해 Azure 진단 확장을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-112">This command enables the Azure Diagnostics extension for all roles.</span></span>

### <span data-ttu-id="fad80-113">예제 2: 지정 된 역할에 대해 Azure 진단 확장 사용</span><span class="sxs-lookup"><span data-stu-id="fad80-113">Example 2: Enable Azure Diagnostics extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole01"
```

<span data-ttu-id="fad80-114">이 명령은 지정 된 역할에 대 한 Azure 진단 확장을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-114">This command enables the Azure Diagnostics extension for a specified role.</span></span>

## <span data-ttu-id="fad80-115">변수</span><span class="sxs-lookup"><span data-stu-id="fad80-115">PARAMETERS</span></span>

### <span data-ttu-id="fad80-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="fad80-116">-CertificateThumbprint</span></span>
<span data-ttu-id="fad80-117">개인 구성을 암호화 하는 데 사용할 인증서 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="fad80-118">이 인증서는 인증서 저장소에 이미 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="fad80-119">인증서를 지정 하지 않으면이 cmdlet은 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fad80-120">-DiagnosticsConfiguration</span><span class="sxs-lookup"><span data-stu-id="fad80-120">-DiagnosticsConfiguration</span></span>
<span data-ttu-id="fad80-121">Azure Diagnostics에 대 한 구성 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-121">Specifies an array of configuration for Azure Diagnostics.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: SetExtensionUsingDiagnosticsConfiguration
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fad80-122">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="fad80-122">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="fad80-123">Azure Diagnostics에 대 한 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-123">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="fad80-124">다음 명령을 사용 하 여 스키마를 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-124">You can download the schema by using the following command:</span></span> 

`(Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'`

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fad80-125">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="fad80-125">-ExtensionId</span></span>
<span data-ttu-id="fad80-126">확장명 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-126">Specifies the extension ID</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fad80-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fad80-127">-InformationAction</span></span>
<span data-ttu-id="fad80-128">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fad80-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fad80-130">하기로</span><span class="sxs-lookup"><span data-stu-id="fad80-130">Continue</span></span>
- <span data-ttu-id="fad80-131">숨기기</span><span class="sxs-lookup"><span data-stu-id="fad80-131">Ignore</span></span>
- <span data-ttu-id="fad80-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="fad80-132">Inquire</span></span>
- <span data-ttu-id="fad80-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fad80-133">SilentlyContinue</span></span>
- <span data-ttu-id="fad80-134">중지가</span><span class="sxs-lookup"><span data-stu-id="fad80-134">Stop</span></span>
- <span data-ttu-id="fad80-135">대기</span><span class="sxs-lookup"><span data-stu-id="fad80-135">Suspend</span></span>

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

### <span data-ttu-id="fad80-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fad80-136">-InformationVariable</span></span>
<span data-ttu-id="fad80-137">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fad80-138">-프로필</span><span class="sxs-lookup"><span data-stu-id="fad80-138">-Profile</span></span>
<span data-ttu-id="fad80-139">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fad80-140">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fad80-141">-역할</span><span class="sxs-lookup"><span data-stu-id="fad80-141">-Role</span></span>
<span data-ttu-id="fad80-142">Azure 진단 구성을 지정할 선택적 역할의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-142">Specifies an optional array of roles for which to specify the Azure Diagnostics configuration.</span></span>
<span data-ttu-id="fad80-143">이 매개 변수를 지정 하지 않으면 진단 구성이 모든 역할에 대 한 기본 구성으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-143">If you do not specify this parameter, the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fad80-144">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fad80-144">-ServiceName</span></span>
<span data-ttu-id="fad80-145">배포의 Azure 서비스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-145">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="fad80-146">-슬롯</span><span class="sxs-lookup"><span data-stu-id="fad80-146">-Slot</span></span>
<span data-ttu-id="fad80-147">수정할 배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-147">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="fad80-148">이 매개 변수에 허용 되는 값은 프로덕션 또는 스테이징입니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-148">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="fad80-149">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="fad80-149">-StorageAccountEndpoint</span></span>
<span data-ttu-id="fad80-150">저장소 계정 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-150">Specifies a storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fad80-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="fad80-151">-StorageAccountKey</span></span>
<span data-ttu-id="fad80-152">저장소 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-152">Specifies a storage account key.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fad80-153">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fad80-153">-StorageAccountName</span></span>
<span data-ttu-id="fad80-154">저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-154">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fad80-155">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="fad80-155">-StorageContext</span></span>
<span data-ttu-id="fad80-156">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-156">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fad80-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="fad80-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="fad80-158">지문과 함께 인증서를 식별 하는 데 사용 되는 손도장 해시 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-158">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="fad80-159">이 매개 변수는 선택 사항이 며 기본값은 sha1입니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-159">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fad80-160">-버전</span><span class="sxs-lookup"><span data-stu-id="fad80-160">-Version</span></span>
<span data-ttu-id="fad80-161">확장의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-161">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fad80-162">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="fad80-162">-X509Certificate</span></span>
<span data-ttu-id="fad80-163">지정 된 경우 x.509 인증서를 지정 하 여 클라우드 서비스에 자동으로 업로드 하 고 확장 개인 구성을 암호화 하는 데 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-163">Specifies an X.509 certificate that, when specified, is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="fad80-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fad80-164">CommonParameters</span></span>
<span data-ttu-id="fad80-165">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad80-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fad80-166">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fad80-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fad80-167">입력</span><span class="sxs-lookup"><span data-stu-id="fad80-167">INPUTS</span></span>

## <span data-ttu-id="fad80-168">출력</span><span class="sxs-lookup"><span data-stu-id="fad80-168">OUTPUTS</span></span>

## <span data-ttu-id="fad80-169">상속자</span><span class="sxs-lookup"><span data-stu-id="fad80-169">NOTES</span></span>

## <span data-ttu-id="fad80-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fad80-170">RELATED LINKS</span></span>

[<span data-ttu-id="fad80-171">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fad80-171">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="fad80-172">제거-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fad80-172">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)


