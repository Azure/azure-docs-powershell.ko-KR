---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 021D4624-AE78-4FBE-B1DE-A8A84DF1FC90
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c3a26887e42884025234ba5f1a7330c258e903
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046045"
---
# <span data-ttu-id="ea37e-101">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="ea37e-101">Set-AzureVMChefExtension</span></span>

## <span data-ttu-id="ea37e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea37e-102">SYNOPSIS</span></span>
<span data-ttu-id="ea37e-103">가상 컴퓨터에 요리사 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-103">Adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="ea37e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea37e-104">SYNTAX</span></span>

### <span data-ttu-id="ea37e-105">Windows (기본값)</span><span class="sxs-lookup"><span data-stu-id="ea37e-105">Windows (Default)</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Windows]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ea37e-106">Linux</span><span class="sxs-lookup"><span data-stu-id="ea37e-106">Linux</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Linux]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ea37e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ea37e-107">DESCRIPTION</span></span>
<span data-ttu-id="ea37e-108">**AzureVMChefExtension** cmdlet은 가상 컴퓨터에 요리사 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="ea37e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ea37e-109">EXAMPLES</span></span>

### <span data-ttu-id="ea37e-110">예제 1: Windows 가상 컴퓨터에 요리사 확장 추가</span><span class="sxs-lookup"><span data-stu-id="ea37e-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ClientRb "C:\\client.rb" -RunList "Apache" -Windows;
```

<span data-ttu-id="ea37e-111">이 명령은 Windows 가상 컴퓨터에 요리사 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-111">This command adds a Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="ea37e-112">가상 컴퓨터가 들어오면 요리사를 사용 하 여 부트스트랩 되 고 Apache에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-112">When the virtual machine comes up, it is bootstrapped with Chef and runs Apache on it.</span></span>

### <span data-ttu-id="ea37e-113">예제 2: 부트스트래핑을 사용 하 여 Windows 가상 컴퓨터에 요리사 확장 추가</span><span class="sxs-lookup"><span data-stu-id="ea37e-113">Example 2: Add a Chef extension to a Windows virtual machine with bootstrapping</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows;
```

<span data-ttu-id="ea37e-114">이 명령은 Windows 가상 컴퓨터에 요리사 확장명을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-114">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="ea37e-115">가상 컴퓨터가 시작 되 면 요리사를 사용 하 여 부트스트랩 되 고 Apache를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-115">When the virtual machine launches, it is bootstrapped with Chef and runs Apache on it.</span></span>
<span data-ttu-id="ea37e-116">부트스트래핑 후 가상 컴퓨터는 JSON 형식으로 지정 된 *BootstrapOptions* 를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-116">After bootstrapping, the virtual machine refers to the *BootstrapOptions* specified in JSON format.</span></span>

### <span data-ttu-id="ea37e-117">예제 3: Windows 가상 컴퓨터에 요리사 확장 추가 및 Apache 및 GIT 설치</span><span class="sxs-lookup"><span data-stu-id="ea37e-117">Example 3: Add a Chef extension to a Windows virtual machine and install Apache and GIT</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -ValidationClientName "MyOrg-Validator" -RunList "apache, git" -Windows;
```

<span data-ttu-id="ea37e-118">이 명령은 Windows 가상 컴퓨터에 요리사 확장명을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-118">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="ea37e-119">가상 컴퓨터가 시작 되 면 요리사를 사용 하 여 부트스트랩 되며 Apache 및 GIT이 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-119">When the virtual machine launches, it is bootstrapped with Chef and have Apache and GIT installed.</span></span>
<span data-ttu-id="ea37e-120">Rb를 제공 하지 않는 경우 요리사 서버 URL 및 유효성 검사 클라이언트 이름을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-120">If you do not provide the client.rb, you need to provide the Chef server URL and validation client name.</span></span>

### <span data-ttu-id="ea37e-121">예제 4: Linux 가상 컴퓨터에 요리사 확장 추가</span><span class="sxs-lookup"><span data-stu-id="ea37e-121">Example 4: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -OrganizationName "MyOrg" -Linux;
```

<span data-ttu-id="ea37e-122">이 명령은 Linux 가상 머신에 요리사 확장명을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-122">This command adds the Chef extension to a Linux virtual machine.</span></span>
<span data-ttu-id="ea37e-123">가상 컴퓨터가 시작 되 면 요리사를 사용 하 여 부트스트랩 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-123">When the virtual machine launches, it is bootstrapped with Chef.</span></span>
<span data-ttu-id="ea37e-124">Rb를 제공 하지 않는 경우 요리사 서버 URL 및 조직을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-124">If you do not provide the client.rb, you need to provide the Chef server URL and organization.</span></span>

## <span data-ttu-id="ea37e-125">변수</span><span class="sxs-lookup"><span data-stu-id="ea37e-125">PARAMETERS</span></span>

### <span data-ttu-id="ea37e-126">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="ea37e-126">-BootstrapOptions</span></span>
<span data-ttu-id="ea37e-127">JSON (JavaScript Object Notation) 형식의 부트스트랩 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-127">Specifies bootstrap options in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="ea37e-128">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="ea37e-128">-BootstrapVersion</span></span>
<span data-ttu-id="ea37e-129">확장과 함께 설치 된 요리사 클라이언트의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-129">Specifies the version of the Chef client that is installed together with the extension.</span></span>

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

### <span data-ttu-id="ea37e-130">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="ea37e-130">-ChefDaemonInterval</span></span>
<span data-ttu-id="ea37e-131">요리사가 실행 되는 빈도 (분 단위)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-131">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="ea37e-132">Azure VM에 요리사를 설치 하지 않으려는 경우에는이 필드에서 값을 0으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-132">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea37e-133">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="ea37e-133">-ChefServerUrl</span></span>
<span data-ttu-id="ea37e-134">요리사 서버의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-134">Specifies the URL of the Chef server.</span></span>

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

### <span data-ttu-id="ea37e-135">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="ea37e-135">-ClientRb</span></span>
<span data-ttu-id="ea37e-136">요리사 클라이언트. rb의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-136">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="ea37e-137">-데몬</span><span class="sxs-lookup"><span data-stu-id="ea37e-137">-Daemon</span></span>
<span data-ttu-id="ea37e-138">무인 실행을 요리사 클라이언트 서비스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-138">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="ea37e-139">노드 플랫폼은 Windows 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-139">The node platform should be Windows.</span></span>
<span data-ttu-id="ea37e-140">허용 되는 옵션: ' 없음 ', ' 서비스 ' 및 ' 작업 '.</span><span class="sxs-lookup"><span data-stu-id="ea37e-140">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="ea37e-141">없음-현재 요리사-클라이언트 서비스가 서비스로 구성 되는 것을 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-141">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="ea37e-142">서비스-백그라운드에서 서비스로 자동 실행 되도록 요리사 클라이언트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-142">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="ea37e-143">작업-secheduled 작업으로 백그라운드에서 자동으로 실행 되도록 요리사 클라이언트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-143">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

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

### <span data-ttu-id="ea37e-144">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ea37e-144">-InformationAction</span></span>
<span data-ttu-id="ea37e-145">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-145">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ea37e-146">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea37e-147">하기로</span><span class="sxs-lookup"><span data-stu-id="ea37e-147">Continue</span></span>
- <span data-ttu-id="ea37e-148">숨기기</span><span class="sxs-lookup"><span data-stu-id="ea37e-148">Ignore</span></span>
- <span data-ttu-id="ea37e-149">Inquire</span><span class="sxs-lookup"><span data-stu-id="ea37e-149">Inquire</span></span>
- <span data-ttu-id="ea37e-150">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ea37e-150">SilentlyContinue</span></span>
- <span data-ttu-id="ea37e-151">중지가</span><span class="sxs-lookup"><span data-stu-id="ea37e-151">Stop</span></span>
- <span data-ttu-id="ea37e-152">대기</span><span class="sxs-lookup"><span data-stu-id="ea37e-152">Suspend</span></span>

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

### <span data-ttu-id="ea37e-153">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ea37e-153">-InformationVariable</span></span>
<span data-ttu-id="ea37e-154">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-154">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ea37e-155">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="ea37e-155">-JsonAttribute</span></span>
<span data-ttu-id="ea37e-156">요리사의 첫 번째 실행에 추가할 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-156">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="ea37e-157">예:-JsonAttribute ' {"foo": "bar"} '</span><span class="sxs-lookup"><span data-stu-id="ea37e-157">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="ea37e-158">-Linux</span><span class="sxs-lookup"><span data-stu-id="ea37e-158">-Linux</span></span>
<span data-ttu-id="ea37e-159">이 cmdlet이 Linux 기반 가상 컴퓨터를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-159">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

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

### <span data-ttu-id="ea37e-160">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="ea37e-160">-OrganizationName</span></span>
<span data-ttu-id="ea37e-161">요리사 확장의 조직 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-161">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="ea37e-162">-프로필</span><span class="sxs-lookup"><span data-stu-id="ea37e-162">-Profile</span></span>
<span data-ttu-id="ea37e-163">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-163">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ea37e-164">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-164">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ea37e-165">-RunList</span><span class="sxs-lookup"><span data-stu-id="ea37e-165">-RunList</span></span>
<span data-ttu-id="ea37e-166">요리사 노드 실행 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-166">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="ea37e-167">-비밀</span><span class="sxs-lookup"><span data-stu-id="ea37e-167">-Secret</span></span>
<span data-ttu-id="ea37e-168">데이터 모음 항목 값을 암호화 하 고 암호를 해독 하는 데 사용 되는 암호화 키입니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-168">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="ea37e-169">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="ea37e-169">-SecretFile</span></span>
<span data-ttu-id="ea37e-170">데이터 모음 항목 값을 암호화 하 고 해독 하는 데 사용 되는 암호화 키가 포함 된 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-170">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="ea37e-171">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="ea37e-171">-ValidationClientName</span></span>
<span data-ttu-id="ea37e-172">유효성 검사 클라이언트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-172">Specifies the name of the validation client.</span></span>

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

### <span data-ttu-id="ea37e-173">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="ea37e-173">-ValidationPem</span></span>
<span data-ttu-id="ea37e-174">요리사 유효성 검사기. pem 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-174">Specifies the Chef validator .pem file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea37e-175">-버전</span><span class="sxs-lookup"><span data-stu-id="ea37e-175">-Version</span></span>
<span data-ttu-id="ea37e-176">요리사 확장명의 버전 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-176">Specifies the version number of the Chef extension.</span></span>

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

### <span data-ttu-id="ea37e-177">-VM</span><span class="sxs-lookup"><span data-stu-id="ea37e-177">-VM</span></span>
<span data-ttu-id="ea37e-178">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-178">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="ea37e-179">-Windows</span><span class="sxs-lookup"><span data-stu-id="ea37e-179">-Windows</span></span>
<span data-ttu-id="ea37e-180">이 cmdlet이 Windows 가상 컴퓨터를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-180">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="ea37e-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea37e-181">CommonParameters</span></span>
<span data-ttu-id="ea37e-182">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea37e-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea37e-183">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea37e-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea37e-184">입력</span><span class="sxs-lookup"><span data-stu-id="ea37e-184">INPUTS</span></span>

## <span data-ttu-id="ea37e-185">출력</span><span class="sxs-lookup"><span data-stu-id="ea37e-185">OUTPUTS</span></span>

## <span data-ttu-id="ea37e-186">상속자</span><span class="sxs-lookup"><span data-stu-id="ea37e-186">NOTES</span></span>

## <span data-ttu-id="ea37e-187">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea37e-187">RELATED LINKS</span></span>

[<span data-ttu-id="ea37e-188">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="ea37e-188">Get-AzureVMChefExtension</span></span>](./Get-AzureVMChefExtension.md)

[<span data-ttu-id="ea37e-189">제거-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="ea37e-189">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)


