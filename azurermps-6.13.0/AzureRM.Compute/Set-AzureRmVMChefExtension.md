---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMChefExtension.md
ms.openlocfilehash: 25082cbf5b69867953580cb0f4b0ea74c15005da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530397"
---
# <span data-ttu-id="44114-101">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="44114-101">Set-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="44114-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44114-102">SYNOPSIS</span></span>
<span data-ttu-id="44114-103">가상 컴퓨터에 요리사 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-103">Adds a Chef extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44114-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44114-104">SYNTAX</span></span>

### <span data-ttu-id="44114-105">Linux</span><span class="sxs-lookup"><span data-stu-id="44114-105">Linux</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44114-106">창을</span><span class="sxs-lookup"><span data-stu-id="44114-106">Windows</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44114-107">설명은</span><span class="sxs-lookup"><span data-stu-id="44114-107">DESCRIPTION</span></span>
<span data-ttu-id="44114-108">**AzureVMChefExtension** cmdlet은 가상 컴퓨터에 요리사 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="44114-109">예제의</span><span class="sxs-lookup"><span data-stu-id="44114-109">EXAMPLES</span></span>

### <span data-ttu-id="44114-110">예제 1: Windows 가상 컴퓨터에 요리사 확장 추가</span><span class="sxs-lookup"><span data-stu-id="44114-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="44114-111">이 명령은 WindowsVM001 이라는 Windows 가상 컴퓨터에 요리사 확장명을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="44114-112">가상 컴퓨터가 시작 되 면 가상 컴퓨터를 bootstraps 요리사 Apache를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="44114-113">예제 2: Linux 가상 컴퓨터에 요리사 확장 추가</span><span class="sxs-lookup"><span data-stu-id="44114-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="44114-114">이 명령은 요리사 확장명을 LinuxVM001 이라는 Linux 가상 컴퓨터에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="44114-115">가상 컴퓨터가 시작 되 면 가상 컴퓨터를 bootstraps 요리사 Apache를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="44114-116">예제 3: 부트스트랩 옵션을 사용 하 여 Windows 가상 컴퓨터에 요리사 확장 추가</span><span class="sxs-lookup"><span data-stu-id="44114-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="44114-117">이 명령은 요리사 확장명을 WindowsVM002 이라는 Windows 가상 컴퓨터에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="44114-118">가상 컴퓨터가 시작 되 면 가상 컴퓨터를 bootstraps 요리사 Apache를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="44114-119">부트스트래핑 후 가상 컴퓨터는 JSON 형식으로 지정 된 BootstrapOptions를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="44114-120">변수</span><span class="sxs-lookup"><span data-stu-id="44114-120">PARAMETERS</span></span>

### <span data-ttu-id="44114-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="44114-121">-AutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="44114-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="44114-122">-BootstrapOptions</span></span>
<span data-ttu-id="44114-123">Client_rb 옵션에서 구성 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-123">Specifies configuration settings in the client_rb option.</span></span>

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

### <span data-ttu-id="44114-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="44114-124">-BootstrapVersion</span></span>
<span data-ttu-id="44114-125">부트스트랩 구성의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-125">Specifies the version of the bootstrap configuration.</span></span>

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

### <span data-ttu-id="44114-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="44114-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="44114-127">요리사가 실행 되는 빈도 (분 단위)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="44114-128">Azure VM에 요리사를 설치 하지 않으려는 경우에는이 필드에서 값을 0으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

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

### <span data-ttu-id="44114-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="44114-129">-ChefServerUrl</span></span>
<span data-ttu-id="44114-130">요리사 서버 링크를 URL로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-130">Specifies the Chef server link, as a URL.</span></span>

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

### <span data-ttu-id="44114-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="44114-131">-ClientRb</span></span>
<span data-ttu-id="44114-132">요리사 클라이언트. rb의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-132">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="44114-133">-데몬</span><span class="sxs-lookup"><span data-stu-id="44114-133">-Daemon</span></span>
<span data-ttu-id="44114-134">무인 실행을 요리사 클라이언트 서비스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="44114-135">노드 플랫폼은 Windows 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-135">The node platform should be Windows.</span></span>
<span data-ttu-id="44114-136">허용 되는 옵션: ' 없음 ', ' 서비스 ' 및 ' 작업 '.</span><span class="sxs-lookup"><span data-stu-id="44114-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="44114-137">없음-현재 요리사-클라이언트 서비스가 서비스로 구성 되는 것을 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="44114-138">서비스-백그라운드에서 서비스로 자동 실행 되도록 요리사 클라이언트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="44114-139">작업-secheduled 작업으로 백그라운드에서 자동으로 실행 되도록 요리사 클라이언트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-139">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

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

### <span data-ttu-id="44114-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44114-140">-DefaultProfile</span></span>
<span data-ttu-id="44114-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44114-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44114-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="44114-142">-JsonAttribute</span></span>
<span data-ttu-id="44114-143">요리사의 첫 번째 실행에 추가할 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="44114-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="44114-144">예:-JsonAttribute ' {"foo": "bar"} '</span><span class="sxs-lookup"><span data-stu-id="44114-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="44114-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="44114-145">-Linux</span></span>
<span data-ttu-id="44114-146">이 cmdlet이 Windows 가상 컴퓨터를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="44114-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="44114-147">-위치</span><span class="sxs-lookup"><span data-stu-id="44114-147">-Location</span></span>
<span data-ttu-id="44114-148">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-148">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="44114-149">-이름</span><span class="sxs-lookup"><span data-stu-id="44114-149">-Name</span></span>
<span data-ttu-id="44114-150">요리사 확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-150">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="44114-151">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="44114-151">-OrganizationName</span></span>
<span data-ttu-id="44114-152">요리사 확장의 조직 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-152">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="44114-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44114-153">-ResourceGroupName</span></span>
<span data-ttu-id="44114-154">가상 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-154">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="44114-155">-RunList</span><span class="sxs-lookup"><span data-stu-id="44114-155">-RunList</span></span>
<span data-ttu-id="44114-156">요리사 노드 실행 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-156">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="44114-157">-비밀</span><span class="sxs-lookup"><span data-stu-id="44114-157">-Secret</span></span>
<span data-ttu-id="44114-158">데이터 모음 항목 값을 암호화 하 고 암호를 해독 하는 데 사용 되는 암호화 키입니다.</span><span class="sxs-lookup"><span data-stu-id="44114-158">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="44114-159">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="44114-159">-SecretFile</span></span>
<span data-ttu-id="44114-160">데이터 모음 항목 값을 암호화 하 고 해독 하는 데 사용 되는 암호화 키가 포함 된 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="44114-160">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="44114-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="44114-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="44114-162">이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-162">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="44114-163">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="44114-163">-ValidationClientName</span></span>
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

### <span data-ttu-id="44114-164">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="44114-164">-ValidationPem</span></span>
<span data-ttu-id="44114-165">요리사 유효성 검사기. pem 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-165">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="44114-166">-VMName</span><span class="sxs-lookup"><span data-stu-id="44114-166">-VMName</span></span>
<span data-ttu-id="44114-167">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-167">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="44114-168">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 요리사 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-168">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="44114-169">-Windows</span><span class="sxs-lookup"><span data-stu-id="44114-169">-Windows</span></span>
<span data-ttu-id="44114-170">이 cmdlet이 Windows 가상 컴퓨터를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="44114-170">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="44114-171">-확인</span><span class="sxs-lookup"><span data-stu-id="44114-171">-Confirm</span></span>
<span data-ttu-id="44114-172">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44114-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44114-173">-WhatIf</span></span>
<span data-ttu-id="44114-174">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="44114-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44114-175">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44114-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44114-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44114-176">CommonParameters</span></span>
<span data-ttu-id="44114-177">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44114-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44114-178">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44114-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44114-179">입력</span><span class="sxs-lookup"><span data-stu-id="44114-179">INPUTS</span></span>

### <span data-ttu-id="44114-180">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="44114-180">System.String</span></span>

### <span data-ttu-id="44114-181">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="44114-181">System.Boolean</span></span>

## <span data-ttu-id="44114-182">출력</span><span class="sxs-lookup"><span data-stu-id="44114-182">OUTPUTS</span></span>

### <span data-ttu-id="44114-183">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="44114-183">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="44114-184">상속자</span><span class="sxs-lookup"><span data-stu-id="44114-184">NOTES</span></span>

## <span data-ttu-id="44114-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44114-185">RELATED LINKS</span></span>

[<span data-ttu-id="44114-186">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="44114-186">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="44114-187">제거-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="44114-187">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)