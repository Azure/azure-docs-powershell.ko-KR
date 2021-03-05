---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 3baa4a20d6109d2767dee1b4ff53e2b363adfccf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968139"
---
# <span data-ttu-id="0cae7-101">Update-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="0cae7-101">Update-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="0cae7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cae7-102">SYNOPSIS</span></span>
<span data-ttu-id="0cae7-103">제공된 선택적 수정자에 대한 ANF(Azure NetApp Files) 활성 디렉터리 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0cae7-103">Updates an Azure NetApp Files (ANF) active directory configuration to the optional modifiers provided.</span></span>

## <span data-ttu-id="0cae7-104">구문</span><span class="sxs-lookup"><span data-stu-id="0cae7-104">SYNTAX</span></span>

### <span data-ttu-id="0cae7-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0cae7-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>] [-Site <String>] [-SmbServerName <String>]
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cae7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cae7-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>]
 [-Site <String>] [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cae7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cae7-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory [-Dns <String[]>] [-Domain <String>] [-Site <String>]
 [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>]
 [-KdcIP <String>] [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -InputObject <PSNetAppFilesActiveDirectory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0cae7-108">설명</span><span class="sxs-lookup"><span data-stu-id="0cae7-108">DESCRIPTION</span></span>
<span data-ttu-id="0cae7-109">**Update-AzNetAppFilesAccount** cmdlet은 ANF 활성 디렉터리 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="0cae7-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF active directory configuration.</span></span>

## <span data-ttu-id="0cae7-110">예제</span><span class="sxs-lookup"><span data-stu-id="0cae7-110">EXAMPLES</span></span>

### <span data-ttu-id="0cae7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0cae7-111">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesActiveDirectory  -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName" -Username $adUsername
```

<span data-ttu-id="0cae7-112">이 명령은 제공된 사용자 이름을 수정하는 주어진 활성 디렉터리 구성에서 업데이트를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="0cae7-112">This command performs an update on the given active directory configuration modifying the username to that provided.</span></span>

## <span data-ttu-id="0cae7-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0cae7-113">PARAMETERS</span></span>

### <span data-ttu-id="0cae7-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0cae7-114">-AccountName</span></span>
<span data-ttu-id="0cae7-115">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="0cae7-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="0cae7-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="0cae7-116">-AccountObject</span></span>
<span data-ttu-id="0cae7-117">활성 디렉터리 개체에 대한 계정</span><span class="sxs-lookup"><span data-stu-id="0cae7-117">The account for the active directory object</span></span>

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

### <span data-ttu-id="0cae7-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="0cae7-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="0cae7-119">ANF 활성 디렉터리의 ID</span><span class="sxs-lookup"><span data-stu-id="0cae7-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cae7-120">-AdName</span><span class="sxs-lookup"><span data-stu-id="0cae7-120">-AdName</span></span>
<span data-ttu-id="0cae7-121">활성 디렉터리 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0cae7-121">Name of the active directory machine.</span></span>
<span data-ttu-id="0cae7-122">이 선택적 매개 변수는 kerberos 볼륨을 만드는 동안에만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0cae7-122">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="0cae7-123">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="0cae7-123">-BackupOperator</span></span>
<span data-ttu-id="0cae7-124">기본 제공 Backup 연산자 활성 디렉터리 그룹에 추가할 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="0cae7-124">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="0cae7-125">도메인 지정자 없이 고유한 사용자 이름 목록</span><span class="sxs-lookup"><span data-stu-id="0cae7-125">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="0cae7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cae7-126">-DefaultProfile</span></span>
<span data-ttu-id="0cae7-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0cae7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cae7-128">-Dns</span><span class="sxs-lookup"><span data-stu-id="0cae7-128">-Dns</span></span>
<span data-ttu-id="0cae7-129">Active Directory 도메인에 대한 DNS 서버 IP 주소 목록(IPv4만 해당)</span><span class="sxs-lookup"><span data-stu-id="0cae7-129">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="0cae7-130">-Domain</span><span class="sxs-lookup"><span data-stu-id="0cae7-130">-Domain</span></span>
<span data-ttu-id="0cae7-131">Active Directory 도메인 이름</span><span class="sxs-lookup"><span data-stu-id="0cae7-131">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="0cae7-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0cae7-132">-InputObject</span></span>
<span data-ttu-id="0cae7-133">제거할 활성 디렉터리 개체</span><span class="sxs-lookup"><span data-stu-id="0cae7-133">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cae7-134">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="0cae7-134">-KdcIP</span></span>
<span data-ttu-id="0cae7-135">활성 디렉터리 머신에 대한 kdc 서버 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="0cae7-135">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="0cae7-136">이 선택적 매개 변수는 kerberos 볼륨을 만드는 동안에만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0cae7-136">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="0cae7-137">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="0cae7-137">-OrganizationalUnit</span></span>
<span data-ttu-id="0cae7-138">Windows Active Directory 내의 OU(조직 단위)</span><span class="sxs-lookup"><span data-stu-id="0cae7-138">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="0cae7-139">-Password</span><span class="sxs-lookup"><span data-stu-id="0cae7-139">-Password</span></span>
<span data-ttu-id="0cae7-140">Active Directory 도메인 관리자의 일반 텍스트 암호, 응답에서 값이 마스킹됩니다.</span><span class="sxs-lookup"><span data-stu-id="0cae7-140">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="0cae7-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cae7-141">-ResourceGroupName</span></span>
<span data-ttu-id="0cae7-142">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="0cae7-142">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="0cae7-143">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="0cae7-143">-ServerRootCACertificate</span></span>
<span data-ttu-id="0cae7-144">SSL/TLS를 통해 LDAP를 사용하도록 설정하면 LDAP 클라이언트에 base64 인코딩된 Active Directory 인증서 서비스의 자체 서명 루트 CA 인증서가 필요합니다. 이 선택적 매개 변수는 LDAP 사용자 매핑 볼륨이 있는 이중 프로토콜에만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0cae7-144">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="0cae7-145">-Site</span><span class="sxs-lookup"><span data-stu-id="0cae7-145">-Site</span></span>
<span data-ttu-id="0cae7-146">서비스가 도메인 컨트롤러 검색을 제한하는 Active Directory 사이트</span><span class="sxs-lookup"><span data-stu-id="0cae7-146">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="0cae7-147">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="0cae7-147">-SmbServerName</span></span>
<span data-ttu-id="0cae7-148">SMB 서버의 NetBIOS 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0cae7-148">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="0cae7-149">이 이름은 AD에 컴퓨터 계정으로 등록되고 볼륨을 탑재하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0cae7-149">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="0cae7-150">-사용자 이름</span><span class="sxs-lookup"><span data-stu-id="0cae7-150">-Username</span></span>
<span data-ttu-id="0cae7-151">Active Directory 도메인 관리자의 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="0cae7-151">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="0cae7-152">-확인</span><span class="sxs-lookup"><span data-stu-id="0cae7-152">-Confirm</span></span>
<span data-ttu-id="0cae7-153">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0cae7-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cae7-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cae7-154">-WhatIf</span></span>
<span data-ttu-id="0cae7-155">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0cae7-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cae7-156">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0cae7-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cae7-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cae7-157">CommonParameters</span></span>
<span data-ttu-id="0cae7-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0cae7-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cae7-159">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0cae7-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cae7-160">입력</span><span class="sxs-lookup"><span data-stu-id="0cae7-160">INPUTS</span></span>

### <span data-ttu-id="0cae7-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="0cae7-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="0cae7-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="0cae7-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="0cae7-163">출력</span><span class="sxs-lookup"><span data-stu-id="0cae7-163">OUTPUTS</span></span>

### <span data-ttu-id="0cae7-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="0cae7-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="0cae7-165">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0cae7-165">NOTES</span></span>

## <span data-ttu-id="0cae7-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0cae7-166">RELATED LINKS</span></span>
