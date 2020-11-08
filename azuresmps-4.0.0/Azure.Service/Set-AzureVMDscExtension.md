---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 649D0A6C-77CE-4E49-AFF8-DF70ABE9FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bb63ff2ffecc3cab8c7d227d10afdd8374dde2a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047351"
---
# <span data-ttu-id="a99cd-101">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="a99cd-101">Set-AzureVMDscExtension</span></span>

## <span data-ttu-id="a99cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a99cd-102">SYNOPSIS</span></span>
<span data-ttu-id="a99cd-103">가상 컴퓨터에서 DSC 확장을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="a99cd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a99cd-104">SYNTAX</span></span>

```
Set-AzureVMDscExtension [-ReferenceName <String>] [-ConfigurationArgument <Hashtable>]
 [-ConfigurationDataPath <String>] [-ConfigurationArchive] <String> [-ConfigurationName <String>]
 [-ContainerName <String>] [-Force] [-StorageContext <AzureStorageContext>] [-Version <String>]
 [-StorageEndpointSuffix <String>] [-WmfVersion <String>] [-DataCollection <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a99cd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a99cd-105">DESCRIPTION</span></span>
<span data-ttu-id="a99cd-106">**AzureVMDscExtension** cmdlet은 가상 컴퓨터에서 DSC (원하는 상태 구성) 확장을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-106">The **Set-AzureVMDscExtension** cmdlet configures the Desired State Configuration (DSC) extension on a virtual machine.</span></span>

## <span data-ttu-id="a99cd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a99cd-107">EXAMPLES</span></span>

### <span data-ttu-id="a99cd-108">예제 1: 가상 컴퓨터에서 DSC 확장 구성</span><span class="sxs-lookup"><span data-stu-id="a99cd-108">Example 1: Configure the DSC extension on a virtual machine</span></span>
```
PS C:\> Set-AzureVMDscExtension -VM $VM -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Path = 'C:\MyDirectory' }
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Contoso.Compute.BGInfo}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd6
OperationStatus             : OK
```

<span data-ttu-id="a99cd-109">이 명령은 가상 컴퓨터에서 DSC 확장을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-109">This command configures the DSC extension on a virtual machine.</span></span>

<span data-ttu-id="a99cd-110">MyConfiguration.ps1.zip 패키지는 **AzureVMDscConfiguration** 명령을 사용 하 여 이전에 Azure storage에 업로드 되어 있어야 하며 MyConfiguration.ps1 스크립트와이에 종속 된 모듈을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-110">The MyConfiguration.ps1.zip package must have been previously uploaded to Azure storage using the **Publish-AzureVMDscConfiguration** command and includes the MyConfiguration.ps1 script and the modules it depends on.</span></span>

<span data-ttu-id="a99cd-111">MyConfiguration 인수는 실행할 스크립트 내의 특정 DSC 구성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-111">The MyConfiguration argument indicates the specific DSC configuration within the script to execute.</span></span>
<span data-ttu-id="a99cd-112">- *Configurationargument* 매개 변수는 구성 함수에 전달 되는 인수를 사용 하 여 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-112">The - *ConfigurationArgument* parameter specifies a hashtable with the arguments that is passed to the configuration function.</span></span>

### <span data-ttu-id="a99cd-113">예제 2: 구성 데이터 경로를 사용 하 여 가상 컴퓨터에서 DSC 확장 구성</span><span class="sxs-lookup"><span data-stu-id="a99cd-113">Example 2: Configure the DSC extension on a virtual machine using a path to the configuration data</span></span>
```
PS C:\> $VM | Set-AzureVMDscExtension -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Credential = Get-Credential } -ConfigurationDataPath MyConfigurationData.psd1
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Microsoft.Compute.BGInfo, Microsoft.Powershell.DSC}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd7
OperationStatus             : OK
```

<span data-ttu-id="a99cd-114">이 명령은 구성 데이터 경로를 사용 하 여 가상 컴퓨터에서 DSC 확장을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-114">This command configures the DSC extension on a virtual machine using a path to the configuration data.</span></span>

## <span data-ttu-id="a99cd-115">변수</span><span class="sxs-lookup"><span data-stu-id="a99cd-115">PARAMETERS</span></span>

### <span data-ttu-id="a99cd-116">-ConfigurationArchive</span><span class="sxs-lookup"><span data-stu-id="a99cd-116">-ConfigurationArchive</span></span>
<span data-ttu-id="a99cd-117">이전에 게시-AzureVMDscConfiguration에 업로드 한 구성 패키지 (.zip 파일)의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-117">Specifies the name of the configuration package (.zip file) that was previously uploaded by Publish-AzureVMDscConfiguration.</span></span>
<span data-ttu-id="a99cd-118">이 매개 변수는 경로 없이 파일 이름만 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-118">This parameter must specify only the name of the file, without any path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99cd-119">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="a99cd-119">-ConfigurationArgument</span></span>
<span data-ttu-id="a99cd-120">구성 함수에 대 한 인수를 지정 하는 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-120">Specifies a hashtable specifying the arguments to the configuration function.</span></span>
<span data-ttu-id="a99cd-121">키는 매개 변수 이름 및 매개 변수 값에 대 한 값에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-121">The keys correspond to the parameter names and the values to the parameter values.</span></span>

<span data-ttu-id="a99cd-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a99cd-123">기본 형식</span><span class="sxs-lookup"><span data-stu-id="a99cd-123">primitive types</span></span>
- <span data-ttu-id="a99cd-124">이름</span><span class="sxs-lookup"><span data-stu-id="a99cd-124">string</span></span>
- <span data-ttu-id="a99cd-125">배열의</span><span class="sxs-lookup"><span data-stu-id="a99cd-125">array</span></span>
- <span data-ttu-id="a99cd-126">PSCredential</span><span class="sxs-lookup"><span data-stu-id="a99cd-126">PSCredential</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99cd-127">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="a99cd-127">-ConfigurationDataPath</span></span>
<span data-ttu-id="a99cd-128">구성 함수에 대 한 데이터를 지정 하는 psd1 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-128">Specifies the path of a .psd1 file that specifies the data for the configuration function.</span></span>
<span data-ttu-id="a99cd-129">이 파일에는 구성 및 환경 데이터 구분에 설명 된 해시 테이블이 포함 되어야 합니다 https://msdn.microsoft.com/en-us/PowerShell/DSC/configData .</span><span class="sxs-lookup"><span data-stu-id="a99cd-129">This file must contain a hashtable as described in Separating Configuration and Environment Datahttps://msdn.microsoft.com/en-us/PowerShell/DSC/configData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99cd-130">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a99cd-130">-ConfigurationName</span></span>
<span data-ttu-id="a99cd-131">DSC 확장에 의해 호출 되는 구성 스크립트 또는 모듈의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-131">Specifies the name of the configuration script or module that is invoked by the DSC extension.</span></span>

<span data-ttu-id="a99cd-132">이 매개 변수의 값은 *Configurationarchive* 에 패키지 된 스크립트 또는 모듈에 포함 된 구성 함수 중 하나의 이름 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-132">The value of this parameter must be the name of one of the configuration functions contained in the scripts or modules packaged in *ConfigurationArchive*.</span></span>

<span data-ttu-id="a99cd-133">이 cmdlet은 사용자가이 매개 변수를 생략 하 고 확장명을 제외한 경우 *Configurationarchive* 매개 변수에 지정 된 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-133">This cmdlet defaults to the name of the file given by the *ConfigurationArchive* parameter if you omit this parameter, excluding any extension.</span></span>
<span data-ttu-id="a99cd-134">예를 들어 *Configurationarchive* 가 "SalesWebSite.ps1.zip" 이면 *ConfigurationName* 에 대 한 기본값은 "saleswebsite"입니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-134">For instance, if *ConfigurationArchive* is "SalesWebSite.ps1.zip", the default value for *ConfigurationName* is "SalesWebSite".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99cd-135">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a99cd-135">-ContainerName</span></span>
<span data-ttu-id="a99cd-136">*Configurationarchive* 가 있는 Azure storage 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-136">Specifies the name of the Azure storage container where the *ConfigurationArchive* is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99cd-137">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="a99cd-137">-DataCollection</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99cd-138">-Force</span><span class="sxs-lookup"><span data-stu-id="a99cd-138">-Force</span></span>
<span data-ttu-id="a99cd-139">이 cmdlet이 기존 blob을 덮어쓰도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-139">Indicates that this cmdlet overwrites existing blobs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99cd-140">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a99cd-140">-InformationAction</span></span>
<span data-ttu-id="a99cd-141">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a99cd-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a99cd-143">하기로</span><span class="sxs-lookup"><span data-stu-id="a99cd-143">Continue</span></span>
- <span data-ttu-id="a99cd-144">숨기기</span><span class="sxs-lookup"><span data-stu-id="a99cd-144">Ignore</span></span>
- <span data-ttu-id="a99cd-145">Inquire</span><span class="sxs-lookup"><span data-stu-id="a99cd-145">Inquire</span></span>
- <span data-ttu-id="a99cd-146">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a99cd-146">SilentlyContinue</span></span>
- <span data-ttu-id="a99cd-147">중지가</span><span class="sxs-lookup"><span data-stu-id="a99cd-147">Stop</span></span>
- <span data-ttu-id="a99cd-148">대기</span><span class="sxs-lookup"><span data-stu-id="a99cd-148">Suspend</span></span>

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

### <span data-ttu-id="a99cd-149">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a99cd-149">-InformationVariable</span></span>
<span data-ttu-id="a99cd-150">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-150">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a99cd-151">-프로필</span><span class="sxs-lookup"><span data-stu-id="a99cd-151">-Profile</span></span>
<span data-ttu-id="a99cd-152">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a99cd-153">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a99cd-154">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="a99cd-154">-ReferenceName</span></span>
<span data-ttu-id="a99cd-155">확장을 참조 하는 데 사용할 수 있는 사용자 정의 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-155">Specifies a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="a99cd-156">이 매개 변수는 확장이 가상 컴퓨터에 처음 추가 될 때 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-156">This parameter is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="a99cd-157">후속 업데이트의 경우 확장을 업데이트 하는 동안 이전에 사용한 참조 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-157">For subsequent updates, you should specify the previously used reference name while you update the extension.</span></span>
<span data-ttu-id="a99cd-158">확장명에 할당 된 *Referencename* 은 **Get-add-azurevm** cmdlet을 사용 하 여 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-158">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99cd-159">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="a99cd-159">-StorageContext</span></span>
<span data-ttu-id="a99cd-160">구성 스크립트에 액세스 하는 데 사용 되는 보안 설정을 제공 하는 Azure storage 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-160">Specifies the Azure storage context that provides the security settings used to access the configuration script.</span></span>
<span data-ttu-id="a99cd-161">이 컨텍스트는 *ContainerName* 매개 변수에 지정 된 컨테이너에 대 한 읽기 액세스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-161">This context provides read access to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99cd-162">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="a99cd-162">-StorageEndpointSuffix</span></span>
<span data-ttu-id="a99cd-163">모든 저장소 서비스에 대 한 DNS 끝점 접미사 (예, "core.contoso.net")를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-163">Specifies the DNS endpoint suffix for all storage services, for instance, "core.contoso.net".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99cd-164">-버전</span><span class="sxs-lookup"><span data-stu-id="a99cd-164">-Version</span></span>
<span data-ttu-id="a99cd-165">사용할 DSC 확장의 특정 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-165">Specifies the specific version of the DSC extension to use.</span></span>
<span data-ttu-id="a99cd-166">이 매개 변수를 지정 하지 않으면 기본값은 "1. \*"로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-166">The default value is set to "1.\*" if this parameter is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99cd-167">-VM</span><span class="sxs-lookup"><span data-stu-id="a99cd-167">-VM</span></span>
<span data-ttu-id="a99cd-168">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-168">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a99cd-169">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="a99cd-169">-WmfVersion</span></span>
<span data-ttu-id="a99cd-170">가상 컴퓨터에 설치할 WMF (Windows Management Framework) 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-170">Specifies the version of the Windows Management Framework (WMF) to install on the virtual machine.</span></span>
<span data-ttu-id="a99cd-171">DSC 확장은 WMF 업데이트 에서만 사용할 수 있는 DSC 기능에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-171">The DSC Extension depends on DSC features that are only available in the WMF updates.</span></span>
<span data-ttu-id="a99cd-172">이 매개 변수는 가상 컴퓨터에 설치할 업데이트 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-172">This parameter specifies which version of the update to install on the virtual machine.</span></span>
<span data-ttu-id="a99cd-173">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-173">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a99cd-174">4.0.</span><span class="sxs-lookup"><span data-stu-id="a99cd-174">4.0.</span></span>
<span data-ttu-id="a99cd-175">새 버전이 이미 설치 되어 있지 않은 경우 WMF 4.0를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-175">Installs WMF 4.0 unless a newer version is already installed.</span></span>
- <span data-ttu-id="a99cd-176">5.0.</span><span class="sxs-lookup"><span data-stu-id="a99cd-176">5.0.</span></span>
<span data-ttu-id="a99cd-177">WMF 5.0 최신 릴리스를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-177">Installs the latest release of WMF 5.0.</span></span>
- <span data-ttu-id="a99cd-178">비최신.</span><span class="sxs-lookup"><span data-stu-id="a99cd-178">latest.</span></span>
<span data-ttu-id="a99cd-179">최신 WMF, 현재 WMF 5.0을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-179">Installs the latest WMF, currently WMF 5.0.</span></span>

<span data-ttu-id="a99cd-180">기본값은 최신 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-180">The default value is latest.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99cd-181">-확인</span><span class="sxs-lookup"><span data-stu-id="a99cd-181">-Confirm</span></span>
<span data-ttu-id="a99cd-182">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99cd-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a99cd-183">-WhatIf</span></span>
<span data-ttu-id="a99cd-184">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a99cd-185">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-185">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99cd-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a99cd-186">CommonParameters</span></span>
<span data-ttu-id="a99cd-187">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a99cd-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a99cd-188">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a99cd-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a99cd-189">입력</span><span class="sxs-lookup"><span data-stu-id="a99cd-189">INPUTS</span></span>

## <span data-ttu-id="a99cd-190">출력</span><span class="sxs-lookup"><span data-stu-id="a99cd-190">OUTPUTS</span></span>

## <span data-ttu-id="a99cd-191">상속자</span><span class="sxs-lookup"><span data-stu-id="a99cd-191">NOTES</span></span>

## <span data-ttu-id="a99cd-192">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a99cd-192">RELATED LINKS</span></span>

[<span data-ttu-id="a99cd-193">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="a99cd-193">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="a99cd-194">제거-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="a99cd-194">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="a99cd-195">제거-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="a99cd-195">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="a99cd-196">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="a99cd-196">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="a99cd-197">게시-AzureVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a99cd-197">Publish-AzureVMDscConfiguration</span></span>](./Publish-AzureVMDscConfiguration.md)


