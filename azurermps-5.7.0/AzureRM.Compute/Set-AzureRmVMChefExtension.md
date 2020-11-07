---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMChefExtension.md
ms.openlocfilehash: 25ddfd3fcb7d087db493e87bdd9781b2bbb77040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702159"
---
# <span data-ttu-id="6090f-101">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="6090f-101">Set-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="6090f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6090f-102">SYNOPSIS</span></span>
<span data-ttu-id="6090f-103">가상 컴퓨터에 요리사 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-103">Adds a Chef extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6090f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6090f-104">SYNTAX</span></span>

### <span data-ttu-id="6090f-105">Linux</span><span class="sxs-lookup"><span data-stu-id="6090f-105">Linux</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6090f-106">창을</span><span class="sxs-lookup"><span data-stu-id="6090f-106">Windows</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6090f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6090f-107">DESCRIPTION</span></span>
<span data-ttu-id="6090f-108">**AzureVMChefExtension** cmdlet은 가상 컴퓨터에 요리사 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="6090f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6090f-109">EXAMPLES</span></span>

### <span data-ttu-id="6090f-110">예제 1: Windows 가상 컴퓨터에 요리사 확장 추가</span><span class="sxs-lookup"><span data-stu-id="6090f-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="6090f-111">이 명령은 WindowsVM001 이라는 Windows 가상 컴퓨터에 요리사 확장명을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="6090f-112">가상 컴퓨터가 시작 되 면 가상 컴퓨터를 bootstraps 요리사 Apache를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="6090f-113">예제 2: Linux 가상 컴퓨터에 요리사 확장 추가</span><span class="sxs-lookup"><span data-stu-id="6090f-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="6090f-114">이 명령은 요리사 확장명을 LinuxVM001 이라는 Linux 가상 컴퓨터에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="6090f-115">가상 컴퓨터가 시작 되 면 가상 컴퓨터를 bootstraps 요리사 Apache를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="6090f-116">예제 3: 부트스트랩 옵션을 사용 하 여 Windows 가상 컴퓨터에 요리사 확장 추가</span><span class="sxs-lookup"><span data-stu-id="6090f-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="6090f-117">이 명령은 요리사 확장명을 WindowsVM002 이라는 Windows 가상 컴퓨터에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="6090f-118">가상 컴퓨터가 시작 되 면 가상 컴퓨터를 bootstraps 요리사 Apache를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="6090f-119">부트스트래핑 후 가상 컴퓨터는 JSON 형식으로 지정 된 BootstrapOptions를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="6090f-120">변수</span><span class="sxs-lookup"><span data-stu-id="6090f-120">PARAMETERS</span></span>

### <span data-ttu-id="6090f-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="6090f-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6090f-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="6090f-122">-BootstrapOptions</span></span>
<span data-ttu-id="6090f-123">Client_rb 옵션에서 구성 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-123">Specifies configuration settings in the client_rb option.</span></span>

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

### <span data-ttu-id="6090f-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="6090f-124">-BootstrapVersion</span></span>
<span data-ttu-id="6090f-125">부트스트랩 구성의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-125">Specifies the version of the bootstrap configuration.</span></span>

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

### <span data-ttu-id="6090f-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="6090f-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="6090f-127">요리사가 실행 되는 빈도 (분 단위)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="6090f-128">Azure VM에 요리사를 설치 하지 않으려는 경우에는이 필드에서 값을 0으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

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

### <span data-ttu-id="6090f-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="6090f-129">-ChefServerUrl</span></span>
<span data-ttu-id="6090f-130">요리사 서버 링크를 URL로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-130">Specifies the Chef server link, as a URL.</span></span>

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

### <span data-ttu-id="6090f-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="6090f-131">-ClientRb</span></span>
<span data-ttu-id="6090f-132">요리사 클라이언트. rb의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-132">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="6090f-133">-데몬</span><span class="sxs-lookup"><span data-stu-id="6090f-133">-Daemon</span></span>
<span data-ttu-id="6090f-134">무인 실행을 요리사 클라이언트 서비스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="6090f-135">노드 플랫폼은 Windows 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-135">The node platform should be Windows.</span></span>
<span data-ttu-id="6090f-136">허용 되는 옵션: ' 없음 ', ' 서비스 ' 및 ' 작업 '.</span><span class="sxs-lookup"><span data-stu-id="6090f-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="6090f-137">없음-현재 요리사-클라이언트 서비스가 서비스로 구성 되는 것을 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="6090f-138">서비스-백그라운드에서 서비스로 자동 실행 되도록 요리사 클라이언트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="6090f-139">작업-secheduled 작업으로 백그라운드에서 자동으로 실행 되도록 요리사 클라이언트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-139">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6090f-140">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="6090f-140">-JsonAttribute</span></span>
<span data-ttu-id="6090f-141">요리사의 첫 번째 실행에 추가할 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-141">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="6090f-142">예:-JsonAttribute ' {"foo": "bar"} '</span><span class="sxs-lookup"><span data-stu-id="6090f-142">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="6090f-143">-Linux</span><span class="sxs-lookup"><span data-stu-id="6090f-143">-Linux</span></span>
<span data-ttu-id="6090f-144">이 cmdlet이 Windows 가상 컴퓨터를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-144">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="6090f-145">-위치</span><span class="sxs-lookup"><span data-stu-id="6090f-145">-Location</span></span>
<span data-ttu-id="6090f-146">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-146">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="6090f-147">-이름</span><span class="sxs-lookup"><span data-stu-id="6090f-147">-Name</span></span>
<span data-ttu-id="6090f-148">요리사 확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-148">Specifies the name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6090f-149">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="6090f-149">-OrganizationName</span></span>
<span data-ttu-id="6090f-150">요리사 확장의 조직 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-150">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="6090f-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6090f-151">-ResourceGroupName</span></span>
<span data-ttu-id="6090f-152">가상 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-152">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6090f-153">-RunList</span><span class="sxs-lookup"><span data-stu-id="6090f-153">-RunList</span></span>
<span data-ttu-id="6090f-154">요리사 노드 실행 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-154">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="6090f-155">-비밀</span><span class="sxs-lookup"><span data-stu-id="6090f-155">-Secret</span></span>
<span data-ttu-id="6090f-156">데이터 모음 항목 값을 암호화 하 고 암호를 해독 하는 데 사용 되는 암호화 키입니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-156">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="6090f-157">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="6090f-157">-SecretFile</span></span>
<span data-ttu-id="6090f-158">데이터 모음 항목 값을 암호화 하 고 해독 하는 데 사용 되는 암호화 키가 포함 된 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-158">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="6090f-159">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="6090f-159">-TypeHandlerVersion</span></span>
<span data-ttu-id="6090f-160">이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-160">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6090f-161">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="6090f-161">-ValidationClientName</span></span>
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

### <span data-ttu-id="6090f-162">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="6090f-162">-ValidationPem</span></span>
<span data-ttu-id="6090f-163">요리사 유효성 검사기. pem 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-163">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="6090f-164">-VMName</span><span class="sxs-lookup"><span data-stu-id="6090f-164">-VMName</span></span>
<span data-ttu-id="6090f-165">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-165">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="6090f-166">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 요리사 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-166">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6090f-167">-Windows</span><span class="sxs-lookup"><span data-stu-id="6090f-167">-Windows</span></span>
<span data-ttu-id="6090f-168">이 cmdlet이 Windows 가상 컴퓨터를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-168">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="6090f-169">-확인</span><span class="sxs-lookup"><span data-stu-id="6090f-169">-Confirm</span></span>
<span data-ttu-id="6090f-170">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6090f-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6090f-171">-WhatIf</span></span>
<span data-ttu-id="6090f-172">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-172">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6090f-173">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6090f-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6090f-174">CommonParameters</span></span>
<span data-ttu-id="6090f-175">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6090f-176">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6090f-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6090f-177">입력</span><span class="sxs-lookup"><span data-stu-id="6090f-177">INPUTS</span></span>

### <span data-ttu-id="6090f-178">않아야</span><span class="sxs-lookup"><span data-stu-id="6090f-178">None</span></span>
<span data-ttu-id="6090f-179">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6090f-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6090f-180">출력</span><span class="sxs-lookup"><span data-stu-id="6090f-180">OUTPUTS</span></span>

## <span data-ttu-id="6090f-181">상속자</span><span class="sxs-lookup"><span data-stu-id="6090f-181">NOTES</span></span>

## <span data-ttu-id="6090f-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6090f-182">RELATED LINKS</span></span>

[<span data-ttu-id="6090f-183">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="6090f-183">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="6090f-184">제거-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="6090f-184">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)
