---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 9ce36109d0ee7be1c0a513db06a81fb61b926697
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489991"
---
# <span data-ttu-id="5d9e9-101">New-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="5d9e9-101">New-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="5d9e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d9e9-102">SYNOPSIS</span></span>
<span data-ttu-id="5d9e9-103">새 ANF(Azure NetApp Files) Active Directory 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d9e9-103">Creates a new Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="5d9e9-104">구문</span><span class="sxs-lookup"><span data-stu-id="5d9e9-104">SYNTAX</span></span>

### <span data-ttu-id="5d9e9-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5d9e9-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String> [-Dns <String[]>]
 -Domain <String> [-Site <String>] -SmbServerName <String> [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d9e9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d9e9-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesActiveDirectory [-Dns <String[]>] -Domain <String> [-Site <String>] -SmbServerName <String>
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d9e9-107">설명</span><span class="sxs-lookup"><span data-stu-id="5d9e9-107">DESCRIPTION</span></span>
<span data-ttu-id="5d9e9-108">**New-AzNetAppFilesActiveDirectory** cmdlet은 ANF 계정에 대한 새 Active Directory 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d9e9-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new active directory configuration for an ANF account.</span></span>

## <span data-ttu-id="5d9e9-109">예제</span><span class="sxs-lookup"><span data-stu-id="5d9e9-109">EXAMPLES</span></span>

### <span data-ttu-id="5d9e9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5d9e9-110">Example 1</span></span>
```powershell
PS C:\> $pwd_secure_string = Read-Host "Enter a Password" -AsSecureString
PS C:\> New-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyADName" -Username "AdUserName -Password $pwd_secure_string -Domain "AdDomain" -Dns "192.0.2.2" -SmbServerName "AdSmbServerName"
```

<span data-ttu-id="5d9e9-111">이 명령은 promt의 AD 암호를 ANF 계정 "MyAnfAccount"에 대한 새 Active Directory 구성을 시초로 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5d9e9-111">This command gets the AD password from promt into a secreates the new Active Directory configuration for the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="5d9e9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d9e9-112">PARAMETERS</span></span>

### <span data-ttu-id="5d9e9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5d9e9-113">-AccountName</span></span>
<span data-ttu-id="5d9e9-114">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="5d9e9-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d9e9-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="5d9e9-115">-AccountObject</span></span>
<span data-ttu-id="5d9e9-116">새 Backup 정책 개체에 대한 계정</span><span class="sxs-lookup"><span data-stu-id="5d9e9-116">The Account for the new Backup Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d9e9-117">-AdName</span><span class="sxs-lookup"><span data-stu-id="5d9e9-117">-AdName</span></span>
<span data-ttu-id="5d9e9-118">Active Directory 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d9e9-118">Name of the active directory machine.</span></span>
<span data-ttu-id="5d9e9-119">이 선택적 매개 변수는 kerberos 볼륨을 만드는 동안에만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d9e9-119">This optional parameter is used only while creating kerberos volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d9e9-120">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="5d9e9-120">-BackupOperator</span></span>
<span data-ttu-id="5d9e9-121">기본 제공 Backup 운영자 Active Directory 그룹에 추가할 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="5d9e9-121">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="5d9e9-122">도메인 지정자 없는 고유한 사용자 이름 목록</span><span class="sxs-lookup"><span data-stu-id="5d9e9-122">A list of unique usernames without domain specifier</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d9e9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d9e9-123">-DefaultProfile</span></span>
<span data-ttu-id="5d9e9-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d9e9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d9e9-125">-Dns</span><span class="sxs-lookup"><span data-stu-id="5d9e9-125">-Dns</span></span>
<span data-ttu-id="5d9e9-126">Active Directory 도메인에 대한 콤마로 구분된 DNS 서버 IP 주소 목록(IPv4에만 해당)</span><span class="sxs-lookup"><span data-stu-id="5d9e9-126">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d9e9-127">-Domain</span><span class="sxs-lookup"><span data-stu-id="5d9e9-127">-Domain</span></span>
<span data-ttu-id="5d9e9-128">Active Directory 도메인의 이름</span><span class="sxs-lookup"><span data-stu-id="5d9e9-128">Name of the Active Directory domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d9e9-129">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="5d9e9-129">-KdcIP</span></span>
<span data-ttu-id="5d9e9-130">Active Directory 컴퓨터의 kdc 서버 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="5d9e9-130">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="5d9e9-131">이 선택적 매개 변수는 kerberos 볼륨을 만드는 동안에만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d9e9-131">This optional parameter is used only while creating kerberos volume.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d9e9-132">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="5d9e9-132">-OrganizationalUnit</span></span>
<span data-ttu-id="5d9e9-133">Windows Active Directory 내의 OU(조직 구성 단위)</span><span class="sxs-lookup"><span data-stu-id="5d9e9-133">The Organizational Unit (OU) within the Windows Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d9e9-134">-Password</span><span class="sxs-lookup"><span data-stu-id="5d9e9-134">-Password</span></span>
<span data-ttu-id="5d9e9-135">Active Directory 도메인 관리자의 일반 텍스트 암호, 값이 응답에 마스킹됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d9e9-135">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d9e9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d9e9-136">-ResourceGroupName</span></span>
<span data-ttu-id="5d9e9-137">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="5d9e9-137">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d9e9-138">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="5d9e9-138">-ServerRootCACertificate</span></span>
<span data-ttu-id="5d9e9-139">SSL/TLS를 통해 LDAP를 사용하는 경우 LDAP 클라이언트에 base64로 인코딩된 Active Directory Certificate Service의 자체 서명된 루트 CA 인증서가 필요합니다. 이 선택적 매개 변수는 LDAP 사용자 매핑 볼륨이 있는 이중 프로토콜에만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d9e9-139">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d9e9-140">-Site</span><span class="sxs-lookup"><span data-stu-id="5d9e9-140">-Site</span></span>
<span data-ttu-id="5d9e9-141">서비스가 도메인 컨트롤러 검색을 제한하는 Active Directory 사이트</span><span class="sxs-lookup"><span data-stu-id="5d9e9-141">The Active Directory site the service will limit Domain Controller discovery to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d9e9-142">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="5d9e9-142">-SmbServerName</span></span>
<span data-ttu-id="5d9e9-143">SMB 서버의 NetBIOS 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d9e9-143">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="5d9e9-144">이 이름은 AD에서 컴퓨터 계정으로 등록되고 볼륨을 탑재하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d9e9-144">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d9e9-145">-Username</span><span class="sxs-lookup"><span data-stu-id="5d9e9-145">-Username</span></span>
<span data-ttu-id="5d9e9-146">Active Directory 도메인 관리자의 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="5d9e9-146">Username of Active Directory domain administrator</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d9e9-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d9e9-147">-Confirm</span></span>
<span data-ttu-id="5d9e9-148">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d9e9-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d9e9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d9e9-149">-WhatIf</span></span>
<span data-ttu-id="5d9e9-150">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5d9e9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d9e9-151">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d9e9-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d9e9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d9e9-152">CommonParameters</span></span>
<span data-ttu-id="5d9e9-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d9e9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d9e9-154">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5d9e9-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d9e9-155">입력</span><span class="sxs-lookup"><span data-stu-id="5d9e9-155">INPUTS</span></span>

### <span data-ttu-id="5d9e9-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="5d9e9-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="5d9e9-157">출력</span><span class="sxs-lookup"><span data-stu-id="5d9e9-157">OUTPUTS</span></span>

### <span data-ttu-id="5d9e9-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="5d9e9-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="5d9e9-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5d9e9-159">NOTES</span></span>

## <span data-ttu-id="5d9e9-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d9e9-160">RELATED LINKS</span></span>
