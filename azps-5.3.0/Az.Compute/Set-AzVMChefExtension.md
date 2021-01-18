---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: 2821e9404fe4101415aa04a8b0d331b3066563df
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493805"
---
# <span data-ttu-id="4773f-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="4773f-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="4773f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4773f-102">SYNOPSIS</span></span>
<span data-ttu-id="4773f-103">가상 머신에 Chef 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="4773f-104">구문</span><span class="sxs-lookup"><span data-stu-id="4773f-104">SYNTAX</span></span>

### <span data-ttu-id="4773f-105">Linux</span><span class="sxs-lookup"><span data-stu-id="4773f-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4773f-106">Windows</span><span class="sxs-lookup"><span data-stu-id="4773f-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4773f-107">설명</span><span class="sxs-lookup"><span data-stu-id="4773f-107">DESCRIPTION</span></span>
<span data-ttu-id="4773f-108">**Set-AzVMChefExtension** cmdlet은 가상 머신에 Chef 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-108">The **Set-AzVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="4773f-109">예제</span><span class="sxs-lookup"><span data-stu-id="4773f-109">EXAMPLES</span></span>

### <span data-ttu-id="4773f-110">예제 1: Windows 가상 머신에 Chef 확장 추가</span><span class="sxs-lookup"><span data-stu-id="4773f-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="4773f-111">이 명령은 WindowsVM001이라는 Windows 가상 머신에 Chef 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="4773f-112">가상 머신이 시작되면 Chef가 가상 머신을 부트스트랩하여 Apache를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="4773f-113">예제 2: Linux 가상 머신에 Chef 확장 추가</span><span class="sxs-lookup"><span data-stu-id="4773f-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="4773f-114">이 명령은 LinuxVM001이라는 Linux 가상 머신에 Chef 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="4773f-115">가상 머신이 시작되면 Chef가 가상 머신을 부트스트랩하여 Apache를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="4773f-116">예제 3: 부트스트락 옵션을 사용하여 Windows 가상 머신에 Chef 확장 추가</span><span class="sxs-lookup"><span data-stu-id="4773f-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="4773f-117">이 명령은 Chef 확장을 WindowsVM002라는 Windows 가상 머신에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="4773f-118">가상 머신이 시작되면 Chef가 가상 머신을 부트스트랩하여 Apache를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="4773f-119">부트스트래핑 후 가상 머신은 JSON 형식으로 지정된 BootstrapOptions를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="4773f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4773f-120">PARAMETERS</span></span>

### <span data-ttu-id="4773f-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="4773f-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="4773f-122">-BootstrapOptions</span></span>
<span data-ttu-id="4773f-123">다음 옵션에서 구성 설정을 client_rb 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-123">Specifies configuration settings in the client_rb option.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="4773f-124">-BootstrapVersion</span></span>
<span data-ttu-id="4773f-125">부트스트힙 구성의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-125">Specifies the version of the bootstrap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="4773f-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="4773f-127">chef-service가 실행되는 빈도(분)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="4773f-128">Chef-service를 Azure VM에 설치하지 않는 경우 이 필드에서 값을 0으로 설정하세요.</span><span class="sxs-lookup"><span data-stu-id="4773f-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="4773f-129">-ChefServerUrl</span></span>
<span data-ttu-id="4773f-130">Chef 서버 링크를 URL로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-130">Specifies the Chef server link, as a URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="4773f-131">-ClientRb</span></span>
<span data-ttu-id="4773f-132">Chef client.rb의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-132">Specifies the full path of the Chef client.rb.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-133">-Daemon</span><span class="sxs-lookup"><span data-stu-id="4773f-133">-Daemon</span></span>
<span data-ttu-id="4773f-134">무인 실행을 위해 chef-client 서비스를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="4773f-135">노드 플랫폼은 Windows입니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-135">The node platform should be Windows.</span></span>
<span data-ttu-id="4773f-136">허용되는 옵션: 'none','service' 및 'task'.</span><span class="sxs-lookup"><span data-stu-id="4773f-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="4773f-137">none - 현재 chef-client 서비스가 서비스로 구성되지 않도록 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="4773f-138">서비스 - 백그라운드에서 서비스로 자동으로 실행하도록 chef-client를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="4773f-139">task - 백그라운드에서 예약된 작업으로 자동으로 실행하도록 chef-client를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-139">task - Configures the chef-client to run automatically in the background as a scheduled task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4773f-140">-DefaultProfile</span></span>
<span data-ttu-id="4773f-141">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="4773f-142">-JsonAttribute</span></span>
<span data-ttu-id="4773f-143">chef-client의 첫 번째 실행에 추가할 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="4773f-144">예: -JsonAttribute '{"foo" : "bar"}'</span><span class="sxs-lookup"><span data-stu-id="4773f-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="4773f-145">-Linux</span></span>
<span data-ttu-id="4773f-146">이 cmdlet이 Windows 가상 머신을 만드는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-147">-Location</span><span class="sxs-lookup"><span data-stu-id="4773f-147">-Location</span></span>
<span data-ttu-id="4773f-148">가상 머신의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-148">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-149">-Name</span><span class="sxs-lookup"><span data-stu-id="4773f-149">-Name</span></span>
<span data-ttu-id="4773f-150">Chef 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-150">Specifies the name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-151">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4773f-151">-NoWait</span></span>
<span data-ttu-id="4773f-152">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-152">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="4773f-153">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-153">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-154">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="4773f-154">-OrganizationName</span></span>
<span data-ttu-id="4773f-155">Chef 확장의 조직 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-155">Specifies the organization name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4773f-156">-ResourceGroupName</span></span>
<span data-ttu-id="4773f-157">가상 머신을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-157">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-158">-RunList</span><span class="sxs-lookup"><span data-stu-id="4773f-158">-RunList</span></span>
<span data-ttu-id="4773f-159">Chef 노드 실행 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-159">Specifies the Chef node run list.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-160">-Secret</span><span class="sxs-lookup"><span data-stu-id="4773f-160">-Secret</span></span>
<span data-ttu-id="4773f-161">데이터 백 항목 값을 암호화하고 암호 해독하는 데 사용되는 암호화 키입니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-161">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-162">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="4773f-162">-SecretFile</span></span>
<span data-ttu-id="4773f-163">데이터백 항목 값을 암호화하고 암호 해독하는 데 사용되는 암호화 키를 포함하는 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-163">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-164">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="4773f-164">-TypeHandlerVersion</span></span>
<span data-ttu-id="4773f-165">이 가상 머신에 사용할 확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-165">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-166">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="4773f-166">-ValidationClientName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-167">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="4773f-167">-ValidationPem</span></span>
<span data-ttu-id="4773f-168">Chef 유효성 검사기 .pem 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-168">Specifies the Chef validator .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-169">-VMName</span><span class="sxs-lookup"><span data-stu-id="4773f-169">-VMName</span></span>
<span data-ttu-id="4773f-170">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-170">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="4773f-171">이 cmdlet은 이 매개 변수가 지정하는 가상 머신에 대한 Chef 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-171">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-172">-Windows</span><span class="sxs-lookup"><span data-stu-id="4773f-172">-Windows</span></span>
<span data-ttu-id="4773f-173">이 cmdlet이 Windows 가상 머신을 만드는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-173">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-174">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4773f-174">-Confirm</span></span>
<span data-ttu-id="4773f-175">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4773f-176">-WhatIf</span></span>
<span data-ttu-id="4773f-177">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4773f-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4773f-178">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-178">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4773f-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4773f-179">CommonParameters</span></span>
<span data-ttu-id="4773f-180">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4773f-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4773f-181">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4773f-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4773f-182">입력</span><span class="sxs-lookup"><span data-stu-id="4773f-182">INPUTS</span></span>

### <span data-ttu-id="4773f-183">System.String</span><span class="sxs-lookup"><span data-stu-id="4773f-183">System.String</span></span>

### <span data-ttu-id="4773f-184">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4773f-184">System.Boolean</span></span>

## <span data-ttu-id="4773f-185">출력</span><span class="sxs-lookup"><span data-stu-id="4773f-185">OUTPUTS</span></span>

### <span data-ttu-id="4773f-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4773f-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="4773f-187">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4773f-187">NOTES</span></span>

## <span data-ttu-id="4773f-188">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4773f-188">RELATED LINKS</span></span>

[<span data-ttu-id="4773f-189">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="4773f-189">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="4773f-190">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="4773f-190">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)
