---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0B3EF123-8424-4CCA-95E8-01301B70CBDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84db81f51a4f8d0da605917f99e14c1721cd89d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046382"
---
# <span data-ttu-id="4879c-101">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="4879c-101">Add-AzureProvisioningConfig</span></span>

## <span data-ttu-id="4879c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4879c-102">SYNOPSIS</span></span>
<span data-ttu-id="4879c-103">Azure 가상 컴퓨터에 대 한 프로비저닝 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-103">Adds provisioning configuration for an Azure virtual machine.</span></span>

## <span data-ttu-id="4879c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4879c-104">SYNTAX</span></span>

### <span data-ttu-id="4879c-105">Windows (기본값)</span><span class="sxs-lookup"><span data-stu-id="4879c-105">Windows (Default)</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4879c-106">Linux</span><span class="sxs-lookup"><span data-stu-id="4879c-106">Linux</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4879c-107">WindowsDomain</span><span class="sxs-lookup"><span data-stu-id="4879c-107">WindowsDomain</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4879c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4879c-108">DESCRIPTION</span></span>
<span data-ttu-id="4879c-109">**추가-AzureProvisioningConfig** Cmdlet은 Azure 가상 컴퓨터 구성에 프로 비전 구성 정보를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-109">The **Add-AzureProvisioningConfig** cmdlet adds provisioning configuration information to an Azure virtual machine configuration.</span></span>
<span data-ttu-id="4879c-110">구성 개체를 사용 하 여 가상 컴퓨터를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-110">You can use the configuration object to create a virtual machine.</span></span>

<span data-ttu-id="4879c-111">이 cmdlet은 독립 실행형 Windows 서버, Active Directory 도메인에 연결 된 Windows 서버, Linux 기반 서버 등의 다양 한 프로비저닝 구성을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-111">This cmdlet supports different provisioning configurations, including standalone Windows servers, Windows servers joined to an Active Directory domain, and Linux-based servers.</span></span>

<span data-ttu-id="4879c-112">Active Directory 도메인에 가입 된 서버를 만들려면 Active Directory 도메인의 정규화 된 도메인 이름 및 도메인에 대 한 가상 컴퓨터 가입 권한이 있는 사용자의 도메인 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-112">To create an Active Directory domain joined server, specify the fully qualified domain name of the Active Directory domain and the domain credentials of a user who has permission to join the virtual machine to the domain.</span></span>

## <span data-ttu-id="4879c-113">예제의</span><span class="sxs-lookup"><span data-stu-id="4879c-113">EXAMPLES</span></span>

### <span data-ttu-id="4879c-114">예제 1: 독립 실행형 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="4879c-114">Example 1: Create a standalone virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="4879c-115">이 명령은 **새 AzureVMConfig** cmdlet을 사용 하 여 가상 컴퓨터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-115">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="4879c-116">이 명령은 파이프라인 연산자를 사용 하 여 현재 cmdlet에 해당 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-116">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4879c-117">현재 cmdlet은 Windows 운영 체제를 실행 하는 가상 컴퓨터에 대 한 프로 비전 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-117">The current cmdlet adds provisioning configuration for a virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="4879c-118">구성에는 관리자 사용자 이름 및 암호가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-118">The configuration includes the administrator user name and password.</span></span>
<span data-ttu-id="4879c-119">이 명령은 가상 컴퓨터를 만드는 **새 add-azurevm** cmdlet에 구성을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="4879c-120">예제 2: 도메인 가입 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="4879c-120">Example 2: Create a domain joined virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="4879c-121">이 명령은 가상 컴퓨터 구성 개체를 만든 다음 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-121">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="4879c-122">현재 cmdlet은 contoso 도메인과 참가할 가상 컴퓨터에 대 한 프로비저닝 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-122">The current cmdlet adds provisioning configuration for a virtual machine to be joined with the contoso domain.</span></span>
<span data-ttu-id="4879c-123">명령에는 가상 컴퓨터를 도메인에 가입 하는 데 필요한 사용자 이름 및 암호가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-123">The command includes user name and password necessary to join the virtual machine to the domain.</span></span>
<span data-ttu-id="4879c-124">구성에는 사용자가 처음 로그온 할 때 사용자 암호를 변경 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-124">The configuration requires the user to change the user password at the first logon.</span></span>
<span data-ttu-id="4879c-125">이 명령은 프로비저닝 개체를 기반으로 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-125">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="4879c-126">예제 3: Linux 기반 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="4879c-126">Example 3: Create a Linux-based virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="4879c-127">이 명령은 가상 컴퓨터 구성 개체를 만든 다음 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-127">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="4879c-128">현재 cmdlet은 Linux 운영 체제를 실행 하는 가상 컴퓨터에 대 한 프로 비전 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-128">The current cmdlet adds provisioning configuration for a virtual machine that runs the Linux operating system.</span></span>
<span data-ttu-id="4879c-129">구성에는 루트 사용자 이름 및 암호가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-129">The configuration includes the root user name and password.</span></span>
<span data-ttu-id="4879c-130">이 명령은 프로비저닝 개체를 기반으로 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-130">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="4879c-131">예제 4: WinRM 용 인증서를 포함 하는 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="4879c-131">Example 4: Create a virtual machine that includes certificates for WinRM</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="4879c-132">첫 번째 명령은 인증서 저장소에서 인증서를 가져온 다음 $certs 배열 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-132">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="4879c-133">두 번째 명령은 가상 컴퓨터 구성 개체를 만든 다음 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-133">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="4879c-134">현재 cmdlet은 WinRM에 대 한 인증서를 포함 하는 프로비저닝 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-134">The current cmdlet adds provisioning configuration that includes certificates for WinRM.</span></span>
<span data-ttu-id="4879c-135">이 명령은 프로비저닝 개체를 기반으로 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-135">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="4879c-136">예제 5: HTTP를 통해 WinRM을 사용 하도록 설정한 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="4879c-136">Example 5: Create a virtual machine that has WinRM enabled over HTTP</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="4879c-137">이 명령은 가상 컴퓨터 구성 개체를 만든 다음 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-137">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="4879c-138">현재 cmdlet은 HTTP를 통해 WinRM이 설정 된 프로비저닝 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-138">The current cmdlet adds provisioning configuration that has WinRM enabled over HTTP.</span></span>
<span data-ttu-id="4879c-139">이 명령은 프로비저닝 개체를 기반으로 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-139">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="4879c-140">예제 6: HTTPS를 통해 WinRM을 사용 하지 않도록 설정 된 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="4879c-140">Example 6: Create a virtual machine that has WinRM disabled over HTTPS</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="4879c-141">이 명령은 가상 컴퓨터 구성 개체를 만든 다음 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-141">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="4879c-142">현재 cmdlet은 HTTPS를 통해 WinRM을 사용 하지 않도록 설정 하는 프로비저닝 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-142">The current cmdlet adds provisioning configuration that disables WinRM over HTTPS.</span></span>
<span data-ttu-id="4879c-143">이 명령은 프로비저닝 개체를 기반으로 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-143">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="4879c-144">예제 7: 키 내보내기를 사용 하지 않고 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="4879c-144">Example 7: Create a virtual machine with no key export</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="4879c-145">첫 번째 명령은 인증서 저장소에서 인증서를 가져온 다음 $certs 배열 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-145">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="4879c-146">두 번째 명령은 가상 컴퓨터 구성 개체를 만든 다음 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-146">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="4879c-147">현재 cmdlet은 인증서를 포함 하 고 개인 키를 내보내지 않는 가상 컴퓨터에 대 한 프로비저닝 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-147">The current cmdlet adds provisioning configuration for a virtual machine that includes certificates and does not export private keys.</span></span>
<span data-ttu-id="4879c-148">이 명령은 프로비저닝 개체를 기반으로 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-148">The command creates the virtual machine based on the provisioning object.</span></span>

## <span data-ttu-id="4879c-149">변수</span><span class="sxs-lookup"><span data-stu-id="4879c-149">PARAMETERS</span></span>

### <span data-ttu-id="4879c-150">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="4879c-150">-AdminUsername</span></span>
<span data-ttu-id="4879c-151">이 구성이 가상 컴퓨터에 만든 관리자 계정의 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-151">Specifies the user name of the Administrator account that this configuration creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-152">-인증서</span><span class="sxs-lookup"><span data-stu-id="4879c-152">-Certificates</span></span>
<span data-ttu-id="4879c-153">이 구성이 가상 컴퓨터에 설치 하는 인증서 집합을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-153">Specifies a set of certificates that this configuration installs on the virtual machine.</span></span>

```yaml
Type: CertificateSettingList
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-154">-CustomDataFile 접속</span><span class="sxs-lookup"><span data-stu-id="4879c-154">-CustomDataFile</span></span>
<span data-ttu-id="4879c-155">가상 컴퓨터에 대 한 데이터 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-155">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="4879c-156">이 cmdlet은 파일의 내용을 Base64로 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-156">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="4879c-157">파일의 길이는 64 킬로바이트 미만 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-157">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="4879c-158">게스트 운영 체제가 Windows 운영 체제 이면이 구성에서는이 데이터 를%SYSTEMDRIVE%\AzureData\CustomData.bin. 이라는 이진 파일로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-158">If the guest operating system is the Windows operating system, this configuration saves this data as a binary file named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="4879c-159">게스트 운영 체제가 Linux 인 경우이 구성은 ovf-env.xml 파일을 사용 하 여 데이터를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-159">If the guest operating system is Linux, this configuration passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="4879c-160">구성에서는 파일을/var/lib/waagent 디렉터리로 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-160">Configuration copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="4879c-161">또한 에이전트는/var/lib/waagent/CustomData.에 Base64로 인코딩된 데이터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-161">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-162">-Disable자동 업데이트</span><span class="sxs-lookup"><span data-stu-id="4879c-162">-DisableAutomaticUpdates</span></span>
<span data-ttu-id="4879c-163">이 구성이 자동 업데이트를 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-163">Indicates that this configuration disables automatic updates.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-164">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="4879c-164">-DisableGuestAgent</span></span>
<span data-ttu-id="4879c-165">이 구성이이 구성을 통해 IaaS (인프라) 게스트 에이전트로 비활성화 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-165">Indicates that this configuration disables the infrastructure as a service (IaaS) guest agent.</span></span>

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

### <span data-ttu-id="4879c-166">-DisableSSH</span><span class="sxs-lookup"><span data-stu-id="4879c-166">-DisableSSH</span></span>
<span data-ttu-id="4879c-167">이 구성이 SSH를 사용 하지 않도록 설정 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-167">Indicates that this configuration disables SSH.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-168">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="4879c-168">-DisableWinRMHttps</span></span>
<span data-ttu-id="4879c-169">이 구성이 HTTPS에서 WinRM (Windows Remote Management)을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-169">Indicates that this configuration disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="4879c-170">기본적으로, WinRM은 HTTPS를 통해 사용 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-170">By default, WinRM is enabled over HTTPS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-171">-도메인</span><span class="sxs-lookup"><span data-stu-id="4879c-171">-Domain</span></span>
<span data-ttu-id="4879c-172">도메인에 컴퓨터를 추가할 수 있는 권한이 있는 계정의 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-172">Specifies the name of the domain of the account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-173">-DomainPassword</span><span class="sxs-lookup"><span data-stu-id="4879c-173">-DomainPassword</span></span>
<span data-ttu-id="4879c-174">도메인에 컴퓨터를 추가할 수 있는 권한이 있는 사용자 계정의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-174">Specifies the password of the user account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-175">-DomainUserName</span><span class="sxs-lookup"><span data-stu-id="4879c-175">-DomainUserName</span></span>
<span data-ttu-id="4879c-176">도메인에 컴퓨터를 추가할 수 있는 권한이 있는 사용자 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-176">Specifies the name of the user account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-177">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="4879c-177">-EnableWinRMHttp</span></span>
<span data-ttu-id="4879c-178">이 구성을 통해 WinRM over HTTP를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-178">Indicates that this configuration enables WinRM over HTTP.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-179">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4879c-179">-InformationAction</span></span>
<span data-ttu-id="4879c-180">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-180">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4879c-181">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-181">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4879c-182">하기로</span><span class="sxs-lookup"><span data-stu-id="4879c-182">Continue</span></span>
- <span data-ttu-id="4879c-183">숨기기</span><span class="sxs-lookup"><span data-stu-id="4879c-183">Ignore</span></span>
- <span data-ttu-id="4879c-184">Inquire</span><span class="sxs-lookup"><span data-stu-id="4879c-184">Inquire</span></span>
- <span data-ttu-id="4879c-185">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4879c-185">SilentlyContinue</span></span>
- <span data-ttu-id="4879c-186">중지가</span><span class="sxs-lookup"><span data-stu-id="4879c-186">Stop</span></span>
- <span data-ttu-id="4879c-187">대기</span><span class="sxs-lookup"><span data-stu-id="4879c-187">Suspend</span></span>

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

### <span data-ttu-id="4879c-188">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4879c-188">-InformationVariable</span></span>
<span data-ttu-id="4879c-189">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-189">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4879c-190">-JoinDomain</span><span class="sxs-lookup"><span data-stu-id="4879c-190">-JoinDomain</span></span>
<span data-ttu-id="4879c-191">참가할 도메인의 FQDN (정규화 된 도메인 이름)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-191">Specifies the fully qualified domain name (FQDN) of the domain to join.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-192">-Linux</span><span class="sxs-lookup"><span data-stu-id="4879c-192">-Linux</span></span>
<span data-ttu-id="4879c-193">이 구성으로 Linux 구성이 생성 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-193">Indicates that this configuration creates a Linux configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-194">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="4879c-194">-LinuxUser</span></span>
<span data-ttu-id="4879c-195">이 구성이 가상 컴퓨터에 만든 Linux 관리 계정의 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-195">Specifies the user name of the Linux administrative account that this configuration creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-196">-MachineObjectOU</span><span class="sxs-lookup"><span data-stu-id="4879c-196">-MachineObjectOU</span></span>
<span data-ttu-id="4879c-197">구성에서 컴퓨터 계정을 만드는 OU (조직 구성 단위)의 정규화 된 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-197">Specifies the fully qualified name of the organizational unit (OU) in which the configuration creates the computer account.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-198">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="4879c-198">-NoExportPrivateKey</span></span>
<span data-ttu-id="4879c-199">이 구성이 개인 키를 업로드 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-199">Indicates that this configuration does not upload the private key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-200">-없음에 대 한 Dpendpoint</span><span class="sxs-lookup"><span data-stu-id="4879c-200">-NoRDPEndpoint</span></span>
<span data-ttu-id="4879c-201">이 구성이 원격 데스크톱 끝점 없이 가상 컴퓨터를 만들기를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-201">Indicates that this configuration creates a virtual machine without a remote desktop endpoint.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-202">-NoSSHEndpoint</span><span class="sxs-lookup"><span data-stu-id="4879c-202">-NoSSHEndpoint</span></span>
<span data-ttu-id="4879c-203">이 구성이 SSH 끝점 없이 가상 컴퓨터를 만들기를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-203">Indicates that this configuration creates a virtual machine without an SSH endpoint.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-204">-NoSSHPassword</span><span class="sxs-lookup"><span data-stu-id="4879c-204">-NoSSHPassword</span></span>
<span data-ttu-id="4879c-205">이 구성이 SSH 암호 없이 가상 컴퓨터를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-205">Indicates that this configuration creates a virtual machine without an SSH password.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-206">-NoWinRMEndpoint</span><span class="sxs-lookup"><span data-stu-id="4879c-206">-NoWinRMEndpoint</span></span>
<span data-ttu-id="4879c-207">이 구성이 가상 컴퓨터에 대 한 WinRM 끝점을 추가 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-207">Indicates that this configuration does not add a WinRM endpoint for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-208">-암호</span><span class="sxs-lookup"><span data-stu-id="4879c-208">-Password</span></span>
<span data-ttu-id="4879c-209">관리자 계정의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-209">Specifies the password of the administrator account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-210">-프로필</span><span class="sxs-lookup"><span data-stu-id="4879c-210">-Profile</span></span>
<span data-ttu-id="4879c-211">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-211">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4879c-212">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-212">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4879c-213">-ResetPasswordOnFirstLogon</span><span class="sxs-lookup"><span data-stu-id="4879c-213">-ResetPasswordOnFirstLogon</span></span>
<span data-ttu-id="4879c-214">가상 컴퓨터에서 처음 로그온 할 때 사용자가 암호를 변경 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-214">Indicates that the virtual machine requires the user to change the password at the first logon.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-215">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="4879c-215">-SSHKeyPairs</span></span>
<span data-ttu-id="4879c-216">SSH 키 쌍을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-216">Specifies SSH key pairs.</span></span>

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-217">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="4879c-217">-SSHPublicKeys</span></span>
<span data-ttu-id="4879c-218">SSH 공개 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-218">Specifies SSH public keys.</span></span>

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-219">-표준 시간대</span><span class="sxs-lookup"><span data-stu-id="4879c-219">-TimeZone</span></span>
<span data-ttu-id="4879c-220">가상 컴퓨터의 표준 시간대를 지정 합니다 (예: 태평양 표준시 또는 캐나다 중부 표준시).</span><span class="sxs-lookup"><span data-stu-id="4879c-220">Specifies the time zone for the virtual machine, for example, Pacific Standard Time or Canada Central Standard Time.</span></span>

```yaml
Type: String
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-221">-VM</span><span class="sxs-lookup"><span data-stu-id="4879c-221">-VM</span></span>
<span data-ttu-id="4879c-222">가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-222">Specifies a virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-223">-Windows</span><span class="sxs-lookup"><span data-stu-id="4879c-223">-Windows</span></span>
<span data-ttu-id="4879c-224">이 구성으로 Windows 운영 체제를 실행 하는 독립 실행형 가상 컴퓨터가 생성 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-224">Indicates that this configuration creates a standalone virtual machine that runs the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-225">-WindowsDomain</span><span class="sxs-lookup"><span data-stu-id="4879c-225">-WindowsDomain</span></span>
<span data-ttu-id="4879c-226">이 구성으로 Active Directory 도메인에 연결 된 Windows server가 생성 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-226">Indicates that this configuration creates Windows server that is joined to an Active Directory domain.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-227">-WinRMCertificate</span><span class="sxs-lookup"><span data-stu-id="4879c-227">-WinRMCertificate</span></span>
<span data-ttu-id="4879c-228">이 구성이 WinRM 끝점에 연결 하는 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-228">Specifies a certificate that this configuration associates to a WinRM endpoint.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-229">-X509Certificates</span><span class="sxs-lookup"><span data-stu-id="4879c-229">-X509Certificates</span></span>
<span data-ttu-id="4879c-230">호스팅된 서비스에 배포 되는 X509 인증서의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-230">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4879c-231">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4879c-231">CommonParameters</span></span>
<span data-ttu-id="4879c-232">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4879c-232">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4879c-233">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4879c-233">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4879c-234">입력</span><span class="sxs-lookup"><span data-stu-id="4879c-234">INPUTS</span></span>

## <span data-ttu-id="4879c-235">출력</span><span class="sxs-lookup"><span data-stu-id="4879c-235">OUTPUTS</span></span>

## <span data-ttu-id="4879c-236">상속자</span><span class="sxs-lookup"><span data-stu-id="4879c-236">NOTES</span></span>

## <span data-ttu-id="4879c-237">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4879c-237">RELATED LINKS</span></span>

[<span data-ttu-id="4879c-238">뉴욕</span><span class="sxs-lookup"><span data-stu-id="4879c-238">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="4879c-239">새로운 AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="4879c-239">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)


