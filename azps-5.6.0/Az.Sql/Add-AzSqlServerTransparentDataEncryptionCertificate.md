---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: beb51449ea0264defe640ba60ad687be405ab669
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961451"
---
# <span data-ttu-id="70944-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="70944-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="70944-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70944-102">SYNOPSIS</span></span>
<span data-ttu-id="70944-103">해당 인스턴스에 대한 투명한 데이터 SQL Server 추가</span><span class="sxs-lookup"><span data-stu-id="70944-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="70944-104">구문</span><span class="sxs-lookup"><span data-stu-id="70944-104">SYNTAX</span></span>

### <span data-ttu-id="70944-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="70944-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70944-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70944-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70944-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70944-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70944-108">설명</span><span class="sxs-lookup"><span data-stu-id="70944-108">DESCRIPTION</span></span>
<span data-ttu-id="70944-109">이 Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate 인스턴스에 대한 투명한 데이터 암호화 인증서를 SQL Server 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="70944-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="70944-110">예제</span><span class="sxs-lookup"><span data-stu-id="70944-110">EXAMPLES</span></span>

### <span data-ttu-id="70944-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="70944-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="70944-112">리소스 그룹 이름 및 SQL Server 사용하여 sql server에 TDE 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="70944-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="70944-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="70944-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="70944-114">서버 resourceId를 사용하여 서버에 TDE 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="70944-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="70944-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="70944-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="70944-116">리소스 그룹의 모든 SQL 서버에 TDE 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="70944-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="70944-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="70944-117">PARAMETERS</span></span>

### <span data-ttu-id="70944-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70944-118">-DefaultProfile</span></span>
<span data-ttu-id="70944-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70944-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70944-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70944-120">-PassThru</span></span>
<span data-ttu-id="70944-121">성공적인 실행에서 추가된 인증서 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="70944-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="70944-122">-Password</span><span class="sxs-lookup"><span data-stu-id="70944-122">-Password</span></span>
<span data-ttu-id="70944-123">투명한 데이터 암호화 인증서에 대한 암호</span><span class="sxs-lookup"><span data-stu-id="70944-123">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70944-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="70944-124">-PrivateBlob</span></span>
<span data-ttu-id="70944-125">투명한 데이터 암호화 인증서에 대한 개인 Blob</span><span class="sxs-lookup"><span data-stu-id="70944-125">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70944-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70944-126">-ResourceGroupName</span></span>
<span data-ttu-id="70944-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="70944-127">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70944-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="70944-128">-ServerName</span></span>
<span data-ttu-id="70944-129">서버 이름</span><span class="sxs-lookup"><span data-stu-id="70944-129">The Server Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70944-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="70944-130">-SqlServer</span></span>
<span data-ttu-id="70944-131">Sql Server 입력 개체</span><span class="sxs-lookup"><span data-stu-id="70944-131">The sql server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70944-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="70944-132">-SqlServerResourceId</span></span>
<span data-ttu-id="70944-133">Sql Server 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="70944-133">The sql server resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70944-134">-확인</span><span class="sxs-lookup"><span data-stu-id="70944-134">-Confirm</span></span>
<span data-ttu-id="70944-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="70944-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70944-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70944-136">-WhatIf</span></span>
<span data-ttu-id="70944-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="70944-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70944-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70944-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70944-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70944-139">CommonParameters</span></span>
<span data-ttu-id="70944-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="70944-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70944-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70944-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70944-142">입력</span><span class="sxs-lookup"><span data-stu-id="70944-142">INPUTS</span></span>

### <span data-ttu-id="70944-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="70944-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="70944-144">System.String</span><span class="sxs-lookup"><span data-stu-id="70944-144">System.String</span></span>

## <span data-ttu-id="70944-145">출력</span><span class="sxs-lookup"><span data-stu-id="70944-145">OUTPUTS</span></span>

### <span data-ttu-id="70944-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="70944-146">System.Boolean</span></span>

## <span data-ttu-id="70944-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="70944-147">NOTES</span></span>

## <span data-ttu-id="70944-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70944-148">RELATED LINKS</span></span>
