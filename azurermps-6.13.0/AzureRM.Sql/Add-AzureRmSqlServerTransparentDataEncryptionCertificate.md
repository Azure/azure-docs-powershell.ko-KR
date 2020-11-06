---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/Add-AzureRmSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: 333de53ccd3632188100af7f3fcde10e140537c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531936"
---
# <span data-ttu-id="dc663-101">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="dc663-101">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="dc663-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc663-102">SYNOPSIS</span></span>
<span data-ttu-id="dc663-103">지정 된 SQL Server 인스턴스에 대 한 투명 한 데이터 암호화 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc663-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc663-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dc663-104">SYNTAX</span></span>

### <span data-ttu-id="dc663-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="dc663-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc663-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc663-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc663-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc663-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc663-108">설명은</span><span class="sxs-lookup"><span data-stu-id="dc663-108">DESCRIPTION</span></span>
<span data-ttu-id="dc663-109">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate에서 지정 된 SQL Server 인스턴스에 대 한 투명 데이터 암호화 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc663-109">The Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="dc663-110">예제의</span><span class="sxs-lookup"><span data-stu-id="dc663-110">EXAMPLES</span></span>

### <span data-ttu-id="dc663-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="dc663-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzureRmSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="dc663-112">리소스 그룹 이름 및 SQL Server 이름을 사용 하 여 sql server에 TDE 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="dc663-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="dc663-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="dc663-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzureRmSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzureRmSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="dc663-114">서버 resourceId를 사용 하 여 서버에 TDE certificate 추가</span><span class="sxs-lookup"><span data-stu-id="dc663-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="dc663-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="dc663-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzureRmSqlServer | Add-AzureRmSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="dc663-116">리소스 그룹의 모든 sql server에 TDE 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="dc663-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="dc663-117">변수</span><span class="sxs-lookup"><span data-stu-id="dc663-117">PARAMETERS</span></span>

### <span data-ttu-id="dc663-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc663-118">-DefaultProfile</span></span>
<span data-ttu-id="dc663-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc663-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc663-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc663-120">-PassThru</span></span>
<span data-ttu-id="dc663-121">성공적으로 실행 되 면 추가 된 인증서 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc663-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="dc663-122">-암호</span><span class="sxs-lookup"><span data-stu-id="dc663-122">-Password</span></span>
<span data-ttu-id="dc663-123">투명 한 데이터 암호화 인증서의 암호</span><span class="sxs-lookup"><span data-stu-id="dc663-123">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="dc663-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="dc663-124">-PrivateBlob</span></span>
<span data-ttu-id="dc663-125">투명 한 데이터 암호화 인증서 용 개인 blob</span><span class="sxs-lookup"><span data-stu-id="dc663-125">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="dc663-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc663-126">-ResourceGroupName</span></span>
<span data-ttu-id="dc663-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="dc663-127">The Resource Group Name</span></span>

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

### <span data-ttu-id="dc663-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dc663-128">-ServerName</span></span>
<span data-ttu-id="dc663-129">서버 이름</span><span class="sxs-lookup"><span data-stu-id="dc663-129">The Server Name</span></span>

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

### <span data-ttu-id="dc663-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="dc663-130">-SqlServer</span></span>
<span data-ttu-id="dc663-131">Sql server 입력 개체</span><span class="sxs-lookup"><span data-stu-id="dc663-131">The sql server input object</span></span>

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

### <span data-ttu-id="dc663-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="dc663-132">-SqlServerResourceId</span></span>
<span data-ttu-id="dc663-133">Sql server 리소스 id</span><span class="sxs-lookup"><span data-stu-id="dc663-133">The sql server resource id</span></span>

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

### <span data-ttu-id="dc663-134">-확인</span><span class="sxs-lookup"><span data-stu-id="dc663-134">-Confirm</span></span>
<span data-ttu-id="dc663-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc663-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc663-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc663-136">-WhatIf</span></span>
<span data-ttu-id="dc663-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dc663-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc663-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc663-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc663-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc663-139">CommonParameters</span></span>
<span data-ttu-id="dc663-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc663-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc663-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc663-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc663-142">입력</span><span class="sxs-lookup"><span data-stu-id="dc663-142">INPUTS</span></span>

### <span data-ttu-id="dc663-143">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="dc663-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="dc663-144">매개 변수: SqlServer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dc663-144">Parameters: SqlServer (ByValue)</span></span>

### <span data-ttu-id="dc663-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dc663-145">System.String</span></span>

## <span data-ttu-id="dc663-146">출력</span><span class="sxs-lookup"><span data-stu-id="dc663-146">OUTPUTS</span></span>

### <span data-ttu-id="dc663-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="dc663-147">System.Boolean</span></span>

## <span data-ttu-id="dc663-148">상속자</span><span class="sxs-lookup"><span data-stu-id="dc663-148">NOTES</span></span>

## <span data-ttu-id="dc663-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc663-149">RELATED LINKS</span></span>
