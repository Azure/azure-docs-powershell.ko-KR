---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-AzCloudServicePublicIPAddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
ms.openlocfilehash: 2a3b643a9ad9d9c588589003e5edb24ceddc4ae1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181804"
---
# <span data-ttu-id="07b3b-101">Get-AzCloudServicePublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="07b3b-101">Get-AzCloudServicePublicIPAddress</span></span>

## <span data-ttu-id="07b3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07b3b-102">SYNOPSIS</span></span>
<span data-ttu-id="07b3b-103">클라우드 서비스의 공용 IP 주소를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-103">Get the public IP address of a cloud service.</span></span>

## <span data-ttu-id="07b3b-104">구문</span><span class="sxs-lookup"><span data-stu-id="07b3b-104">SYNTAX</span></span>

### <span data-ttu-id="07b3b-105">CloudServiceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="07b3b-105">CloudServiceName (Default)</span></span>
```
Get-AzCloudServicePublicIPAddress -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [<CommonParameters>]
```

### <span data-ttu-id="07b3b-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="07b3b-106">CloudService</span></span>
```
Get-AzCloudServicePublicIPAddress -CloudService <CloudService> [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="07b3b-107">설명</span><span class="sxs-lookup"><span data-stu-id="07b3b-107">DESCRIPTION</span></span>
<span data-ttu-id="07b3b-108">클라우드 서비스의 공용 IP 주소를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-108">Get the public IP address of a cloud service.</span></span>

## <span data-ttu-id="07b3b-109">예제</span><span class="sxs-lookup"><span data-stu-id="07b3b-109">EXAMPLES</span></span>

### <span data-ttu-id="07b3b-110">예제 1: 특정 클라우드 서비스 이름에 대한 인스턴스 수준 공용 IP 주소를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-110">Example 1: Get instance level public IP addresses for a given cloud service name.</span></span>
```powershell
PS C:\> Get-AzCloudServicePublicIPAddress -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="07b3b-111">특정 클라우드 서비스 이름에 대한 인스턴스 수준 공용 IP 주소를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-111">Gets the instance level public IP addresses for a given cloud service name.</span></span>

### <span data-ttu-id="07b3b-112">예제 2: 주어진 클라우드 서비스 개체에 대한 인스턴스 수준 공용 IP 주소를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-112">Example 2: Get instance level public IP addresses for a given cloud service object.</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServicePublicIPAddress -CloudService $cs

```

<span data-ttu-id="07b3b-113">주어진 클라우드 서비스 개체에 대한 인스턴스 수준 공용 IP 주소를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-113">Gets the instance level public IP addresses for a given cloud service object.</span></span>

## <span data-ttu-id="07b3b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07b3b-114">PARAMETERS</span></span>

### <span data-ttu-id="07b3b-115">-CloudService</span><span class="sxs-lookup"><span data-stu-id="07b3b-115">-CloudService</span></span>
<span data-ttu-id="07b3b-116">CloudService 인스턴스.</span><span class="sxs-lookup"><span data-stu-id="07b3b-116">CloudService instance.</span></span>
<span data-ttu-id="07b3b-117">생성을 위해 CLOUDSERVICE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="07b3b-117">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudService
Parameter Sets: CloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b3b-118">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="07b3b-118">-CloudServiceName</span></span>
<span data-ttu-id="07b3b-119">CloudServiceName.</span><span class="sxs-lookup"><span data-stu-id="07b3b-119">CloudServiceName.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b3b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07b3b-120">-ResourceGroupName</span></span>
<span data-ttu-id="07b3b-121">ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="07b3b-121">ResourceGroupName.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b3b-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="07b3b-122">-SubscriptionId</span></span>
<span data-ttu-id="07b3b-123">구독.</span><span class="sxs-lookup"><span data-stu-id="07b3b-123">Subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b3b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07b3b-124">CommonParameters</span></span>
<span data-ttu-id="07b3b-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07b3b-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="07b3b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07b3b-127">입력</span><span class="sxs-lookup"><span data-stu-id="07b3b-127">INPUTS</span></span>

## <span data-ttu-id="07b3b-128">출력</span><span class="sxs-lookup"><span data-stu-id="07b3b-128">OUTPUTS</span></span>

## <span data-ttu-id="07b3b-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="07b3b-129">NOTES</span></span>

<span data-ttu-id="07b3b-130">별칭</span><span class="sxs-lookup"><span data-stu-id="07b3b-130">ALIASES</span></span>

<span data-ttu-id="07b3b-131">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="07b3b-131">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="07b3b-132">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-132">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="07b3b-133">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="07b3b-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="07b3b-134">CLOUDSERVICE: <CloudService> CloudService 인스턴스.</span><span class="sxs-lookup"><span data-stu-id="07b3b-134">CLOUDSERVICE <CloudService>: CloudService instance.</span></span>
  - <span data-ttu-id="07b3b-135">`Location <String>`: 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-135">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="07b3b-136">`[Configuration <String>]`: 클라우드 서비스에 대한 XML 서비스 구성(.cscfg)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-136">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="07b3b-137">`[ConfigurationUrl <String>]`: Blob service에서 서비스 구성의 위치를 참조하는 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-137">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="07b3b-138">서비스 패키지 URL은 모든 저장소 계정에서 SAS(공유 액세스 서명) URI일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-138">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="07b3b-139">쓰기 전용 속성으로 GET 호출에서 반환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-139">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="07b3b-140">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: 클라우드 서비스 확장 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-140">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="07b3b-141">`[Extension <IExtension[]>]`: 클라우드 서비스에 대한 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-141">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="07b3b-142">`[AutoUpgradeMinorVersion <Boolean?>]`: 플랫폼이 사용 가능해질 때 typeHandlerVersion을 더 높은 부 버전으로 자동으로 업그레이드할 수 있는지 여부를 명시적으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-142">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="07b3b-143">`[ForceUpdateTag <String>]`: 제공된 공용 및 보호된 설정을 강제 적용하기 위한 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-143">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="07b3b-144">태그 값을 변경하면 공용 또는 보호된 설정을 변경하지 않고 확장을 다시 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-144">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="07b3b-145">forceUpdateTag가 변경되지 않은 경우 공용 또는 보호된 설정에 대한 업데이트는 처리기에서 계속 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-145">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="07b3b-146">forceUpdateTag 또는 공용 또는 보호된 설정이 변경되지 않는 경우 확장은 동일한 시퀀스 번호의 역할 인스턴스로 흐르며, 다시 실행할지 여부는 처리기 구현에 따라 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-146">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="07b3b-147">`[Name <String>]`: 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-147">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="07b3b-148">`[ProtectedSetting <String>]`: 역할 인스턴스로 보내기 전에 암호화되는 확장에 대한 보호된 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-148">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="07b3b-149">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="07b3b-149">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="07b3b-150">`[Publisher <String>]`: 확장 처리기 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-150">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="07b3b-151">`[RolesAppliedTo <String[]>]`: 이 확장을 적용할 역할의 선택적 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-151">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="07b3b-152">속성이 지정되지 않은 경우 또는 '\*'를 지정하면 클라우드 서비스의 모든 역할에 확장이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-152">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="07b3b-153">`[Setting <String>]`: 확장에 대한 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-153">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="07b3b-154">JSON 확장의 경우 확장에 대한 JSON 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-154">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="07b3b-155">XML 확장(예: RDP)의 경우 확장에 대한 XML 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-155">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="07b3b-156">`[SourceVaultId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="07b3b-156">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="07b3b-157">`[Type <String>]`: 확장의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-157">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="07b3b-158">`[TypeHandlerVersion <String>]`: 확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-158">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="07b3b-159">확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-159">Specifies the version of the extension.</span></span> <span data-ttu-id="07b3b-160">이 요소를 지정하지 않은 경우 또는 값으로 추가(\*)를 사용하는 경우 최신 버전의 확장이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-160">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="07b3b-161">값이 주 버전 번호와 부 버전 번호(X.)로 지정된 경우 지정된 주 버전의 최신 부 버전이 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-161">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="07b3b-162">주 버전 번호와 부 버전 번호(X.Y)가 지정되면 특정 확장 버전이 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-162">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="07b3b-163">버전이 지정된 경우 역할 인스턴스에서 자동 업그레이드가 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-163">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="07b3b-164">`[NetworkProfile <ICloudServiceNetworkProfile>]`: 클라우드 서비스에 대한 네트워크 프로필입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-164">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="07b3b-165">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: 클라우드 서비스에 대한 부하 균형 조정기 구성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-165">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="07b3b-166">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: IP 목록</span><span class="sxs-lookup"><span data-stu-id="07b3b-166">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="07b3b-167">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="07b3b-167">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="07b3b-168">`[PrivateIPAddress <String>]`: 클라우드 서비스에서 참조하는 개인 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-168">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="07b3b-169">`[PublicIPAddressId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="07b3b-169">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="07b3b-170">`[SubnetId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="07b3b-170">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="07b3b-171">`[Name <String>]`: 리소스 이름</span><span class="sxs-lookup"><span data-stu-id="07b3b-171">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="07b3b-172">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="07b3b-172">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="07b3b-173">`[Id <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="07b3b-173">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="07b3b-174">`[OSProfile <ICloudServiceOSProfile>]`: 클라우드 서비스에 대한 OS 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-174">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="07b3b-175">`[Secret <ICloudServiceVaultSecretGroup[]>]`: 역할 인스턴스에 설치해야 하는 인증서 집합을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-175">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="07b3b-176">`[SourceVaultId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="07b3b-176">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="07b3b-177">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: 인증서를 포함하는 SourceVault의 키 자격 증명 모음 참조 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-177">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="07b3b-178">`[CertificateUrl <String>]`: Key Vault에 비밀로 업로드된 인증서의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-178">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="07b3b-179">`[PackageUrl <String>]`: Blob service에서 서비스 패키지의 위치를 참조하는 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-179">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="07b3b-180">서비스 패키지 URL은 모든 저장소 계정에서 SAS(공유 액세스 서명) URI일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-180">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="07b3b-181">쓰기 전용 속성으로 GET 호출에서 반환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-181">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="07b3b-182">`[RoleProfile <ICloudServiceRoleProfile>]`: 클라우드 서비스에 대한 역할 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-182">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="07b3b-183">`[Role <ICloudServiceRoleProfileProperties[]>]`: 클라우드 서비스에 대한 역할 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-183">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="07b3b-184">`[Name <String>]`: 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-184">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="07b3b-185">`[SkuCapacity <Int64?>]`: 클라우드 서비스의 역할 인스턴스 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-185">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="07b3b-186">`[SkuName <String>]`: SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-186">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="07b3b-187">참고: 클라우드 서비스가 현재 있는 하드웨어에서 새 SKU가 지원되지 않는 경우 클라우드 서비스를 삭제하고 다시 새로 고치거나 이전 SKU로 다시 이동해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-187">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="07b3b-188">`[SkuTier <String>]`: 클라우드 서비스의 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-188">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="07b3b-189">가능한 값은</span><span class="sxs-lookup"><span data-stu-id="07b3b-189">Possible Values are</span></span> <br /><br /> <span data-ttu-id="07b3b-190">**표준**</span><span class="sxs-lookup"><span data-stu-id="07b3b-190">**Standard**</span></span> <br /><br /> <span data-ttu-id="07b3b-191">**기본**</span><span class="sxs-lookup"><span data-stu-id="07b3b-191">**Basic**</span></span>
  - <span data-ttu-id="07b3b-192">`[StartCloudService <Boolean?>]`: (선택 사항) 클라우드 서비스를 만든 직후 시작할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-192">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="07b3b-193">기본값은 `true` .</span><span class="sxs-lookup"><span data-stu-id="07b3b-193">The default value is `true`.</span></span>         <span data-ttu-id="07b3b-194">false이면 서비스 모델이 여전히 배포되지만 코드는 즉시 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-194">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="07b3b-195">대신, 서비스가 시작될 때 시작을 호출할 때까지 PoweredOff입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-195">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="07b3b-196">배포된 서비스는 전원이 공급되는 경우에도 요금이 계속 부과됩니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-196">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="07b3b-197">`[Tag <ICloudServiceTags>]`: 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-197">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="07b3b-198">`[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="07b3b-199">`[UpgradeMode <CloudServiceUpgradeMode?>]`: 클라우드 서비스에 대한 업데이트 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-199">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="07b3b-200">역할 인스턴스는 서비스가 배포될 때 도메인을 업데이트하기 위해 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-200">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="07b3b-201">업데이트는 각 업데이트 도메인에서 수동으로 시작하거나 모든 업데이트 도메인에서 자동으로 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-201">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="07b3b-202">가능한 값은</span><span class="sxs-lookup"><span data-stu-id="07b3b-202">Possible Values are</span></span> <br /><br /><span data-ttu-id="07b3b-203">**자동**</span><span class="sxs-lookup"><span data-stu-id="07b3b-203">**Auto**</span></span><br /><br /><span data-ttu-id="07b3b-204">**수동**</span><span class="sxs-lookup"><span data-stu-id="07b3b-204">**Manual**</span></span> <br /><br /><span data-ttu-id="07b3b-205">**동시**</span><span class="sxs-lookup"><span data-stu-id="07b3b-205">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="07b3b-206">지정하지 않으면 기본값은 자동입니다. Manual로 설정된 경우 PUT UpdateDomain을 호출하여 업데이트를 적용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-206">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="07b3b-207">자동으로 설정하면 업데이트가 순서대로 각 업데이트 도메인에 자동으로 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="07b3b-207">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="07b3b-208">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07b3b-208">RELATED LINKS</span></span>

