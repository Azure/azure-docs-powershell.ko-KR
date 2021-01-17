---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: 0e69cfe7ae76be1d79bdd8cf0d7db193a05219d5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337634"
---
# <span data-ttu-id="37a6e-101">New-AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="37a6e-101">New-AzDataFactoryEncryptValue</span></span>

## <span data-ttu-id="37a6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="37a6e-103">중요한 데이터를 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-103">Encrypts sensitive data.</span></span>

## <span data-ttu-id="37a6e-104">구문</span><span class="sxs-lookup"><span data-stu-id="37a6e-104">SYNTAX</span></span>

### <span data-ttu-id="37a6e-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="37a6e-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37a6e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="37a6e-106">ByFactoryObject</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37a6e-107">설명</span><span class="sxs-lookup"><span data-stu-id="37a6e-107">DESCRIPTION</span></span>
<span data-ttu-id="37a6e-108">**New-AzDataFactoryEncryptValue** cmdlet은 암호 또는 Microsoft SQL Server 연결 문자열과 같은 중요한 데이터를 암호화하고 암호화된 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-108">The **New-AzDataFactoryEncryptValue** cmdlet encrypts sensitive data, such as a password or a Microsoft SQL Server connection string, and returns an encrypted value.</span></span>

## <span data-ttu-id="37a6e-109">예제</span><span class="sxs-lookup"><span data-stu-id="37a6e-109">EXAMPLES</span></span>

### <span data-ttu-id="37a6e-110">예제 1: 비 ODBC 연결 문자열 암호화</span><span class="sxs-lookup"><span data-stu-id="37a6e-110">Example 1: Encrypt a non-ODBC connection string</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

<span data-ttu-id="37a6e-111">첫 번째 명령은 ConvertTo-SecureString cmdlet을 사용하여 지정된 연결 문자열을 **SecureString** 개체로 변환한 다음 해당 개체를 $Value 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-111">The first command uses the ConvertTo-SecureString cmdlet to convert the specified connection string to a **SecureString** object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="37a6e-112">자세한 내용은 `Get-Help ConvertTo-SecureString` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-112">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="37a6e-113">허용되는 값: SQL Server 또는 Oracle 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-113">Allowed values: SQL Server or Oracle connection string.</span></span>
<span data-ttu-id="37a6e-114">두 번째 명령은 지정된 데이터 팩터리, 게이트웨이$Value 리소스 그룹 및 연결된 서비스 유형에 대해 $Value 개체에 대해 암호화된 값을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-114">The second command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="37a6e-115">예제 2: Windows 인증을 사용하는 ODBC가 아닌 연결 문자열을 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-115">Example 2: Encrypt a non-ODBC connection string that uses Windows authentication.</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

<span data-ttu-id="37a6e-116">첫 번째 명령은 **ConvertTo-SecureString을** 사용하여 지정된 연결 문자열을 보안 문자열 개체로 변환한 다음 해당 개체를 $Value 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-116">The first command uses **ConvertTo-SecureString** to convert the specified connection string to a secure string object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="37a6e-117">두 번째 명령은 Get-Credential cmdlet을 사용하여 windows 인증(사용자 이름 및 암호)을 수집한 다음 해당 **PSCredential** 개체를 $Credential 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-117">The second command uses the Get-Credential cmdlet to collect the windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="37a6e-118">자세한 내용은 `Get-Help Get-Credential` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-118">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="37a6e-119">세 번째 명령은 지정된 데이터 팩터리, 게이트웨이$Credential 리소스 그룹 및 연결된 서비스 유형에 대해 $Value 및 $Credential 개체에 대해 암호화된 값을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-119">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="37a6e-120">예제 3: 파일 시스템 연결된 서비스에 대한 서버 이름 및 자격 증명 암호화</span><span class="sxs-lookup"><span data-stu-id="37a6e-120">Example 3: Encrypt server name and credentials for File system linked service</span></span>
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

<span data-ttu-id="37a6e-121">첫 번째 명령은 **ConvertTo-SecureString을** 사용하여 지정된 문자열을 보안 문자열로 변환한 다음 해당 개체를 $Value 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-121">The first command uses **ConvertTo-SecureString** to convert the specified string to a secure string, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="37a6e-122">두 번째 명령은 **Get-Credential을** 사용하여 Windows 인증(사용자 이름 및 암호)을 수집한 다음 해당 **PSCredential** 개체를 $Credential 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-122">The second command uses **Get-Credential** to collect the Windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="37a6e-123">세 번째 명령은 지정된 데이터 팩터리, 게이트웨이$Credential 리소스 그룹 및 연결된 서비스 유형에 대해 $Value 및 $Credential 개체에 대해 암호화된 값을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-123">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="37a6e-124">예제 4: HDFS 연결된 서비스에 대한 자격 증명 암호화</span><span class="sxs-lookup"><span data-stu-id="37a6e-124">Example 4: Encrypt credentials for HDFS linked service</span></span>
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

<span data-ttu-id="37a6e-125">**ConvertTo-SecureString** 명령은 지정된 문자열을 보안 문자열로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-125">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="37a6e-126">**New-Object** 명령은 보안 사용자 이름 및 암호 문자열을 사용하여 PSCredential 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-126">The **New-Object** command creates a PSCredential object using the secure username and password strings.</span></span>
<span data-ttu-id="37a6e-127">대신 **Get-Credential** 명령을 사용하여 Windows 인증(사용자 이름 및 암호)을 수집한 다음 이전 예제와 같이 반환된 **PSCredential** 개체를 $credential 변수에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-127">Instead, you could use the **Get-Credential** command to collect Windows authentication (user name and password), and then store the returned **PSCredential** object in the $credential variable as shown in previous examples.</span></span>
<span data-ttu-id="37a6e-128">**New-AzDataFactoryEncryptValue** 명령은 지정된 데이터 팩터리, 게이트웨이$Credential 리소스 그룹 및 연결된 서비스 유형에 대해 $Credential 개체에 대해 암호화된 값을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-128">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="37a6e-129">예제 5: ODBC 연결된 서비스에 대한 자격 증명 암호화</span><span class="sxs-lookup"><span data-stu-id="37a6e-129">Example 5: Encrypt credentials for ODBC linked service</span></span>
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

<span data-ttu-id="37a6e-130">**ConvertTo-SecureString** 명령은 지정된 문자열을 보안 문자열로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-130">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="37a6e-131">**New-AzDataFactoryEncryptValue** 명령은 지정된 데이터 팩터리, 게이트웨이$Value 리소스 그룹 및 연결된 서비스 유형에 대해 $Value 개체에 대해 암호화된 값을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-131">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

## <span data-ttu-id="37a6e-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37a6e-132">PARAMETERS</span></span>

### <span data-ttu-id="37a6e-133">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="37a6e-133">-AuthenticationType</span></span>
<span data-ttu-id="37a6e-134">데이터 원본에 연결하는 데 사용할 인증 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-134">Specifies the type of authentication to be used to connect to the data source.</span></span>
<span data-ttu-id="37a6e-135">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="37a6e-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37a6e-136">Windows</span><span class="sxs-lookup"><span data-stu-id="37a6e-136">Windows</span></span>
- <span data-ttu-id="37a6e-137">기본</span><span class="sxs-lookup"><span data-stu-id="37a6e-137">Basic</span></span>
- <span data-ttu-id="37a6e-138">익명.</span><span class="sxs-lookup"><span data-stu-id="37a6e-138">Anonymous.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37a6e-139">-Credential</span><span class="sxs-lookup"><span data-stu-id="37a6e-139">-Credential</span></span>
<span data-ttu-id="37a6e-140">사용할 Windows 인증 자격 증명(사용자 이름 및 암호)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-140">Specifies the Windows authentication credentials (user name and password) to be used.</span></span>
<span data-ttu-id="37a6e-141">이 cmdlet은 여기에서 지정한 자격 증명 데이터를 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-141">This cmdlet encrypts the credential data you specify here.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37a6e-142">-Database</span><span class="sxs-lookup"><span data-stu-id="37a6e-142">-Database</span></span>
<span data-ttu-id="37a6e-143">연결된 서비스의 데이터베이스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-143">Specifies the database name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37a6e-144">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="37a6e-144">-DataFactory</span></span>
<span data-ttu-id="37a6e-145">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="37a6e-145">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="37a6e-146">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 대한 데이터를 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-146">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37a6e-147">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="37a6e-147">-DataFactoryName</span></span>
<span data-ttu-id="37a6e-148">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-148">Specifies the name of a data factory.</span></span>
<span data-ttu-id="37a6e-149">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 대한 데이터를 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-149">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37a6e-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37a6e-150">-DefaultProfile</span></span>
<span data-ttu-id="37a6e-151">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="37a6e-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37a6e-152">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="37a6e-152">-GatewayName</span></span>
<span data-ttu-id="37a6e-153">게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-153">Specifies the name of the gateway.</span></span>
<span data-ttu-id="37a6e-154">이 cmdlet은 이 매개 변수가 지정하는 게이트웨이에 대한 데이터를 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-154">This cmdlet encrypts data for the gateway that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37a6e-155">-NonCredentialValue</span><span class="sxs-lookup"><span data-stu-id="37a6e-155">-NonCredentialValue</span></span>
<span data-ttu-id="37a6e-156">ODBC(Open Database Connectivity) 연결 문자열의 비 자격 증명 부분을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-156">Specifies the non-credential part of the Open Database Connectivity (ODBC) connection string.</span></span>
<span data-ttu-id="37a6e-157">이 매개 변수는 ODBC 연결된 서비스에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-157">This parameter is applicable only for the ODBC linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37a6e-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37a6e-158">-ResourceGroupName</span></span>
<span data-ttu-id="37a6e-159">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-159">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="37a6e-160">이 cmdlet은 이 매개 변수가 지정하는 그룹에 대한 데이터를 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-160">This cmdlet encrypts data for the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37a6e-161">-Server</span><span class="sxs-lookup"><span data-stu-id="37a6e-161">-Server</span></span>
<span data-ttu-id="37a6e-162">연결된 서비스의 서버 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-162">Specifies the server name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37a6e-163">-Type</span><span class="sxs-lookup"><span data-stu-id="37a6e-163">-Type</span></span>
<span data-ttu-id="37a6e-164">연결된 서비스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-164">Specifies the linked service type.</span></span>
<span data-ttu-id="37a6e-165">이 cmdlet은 이 매개 변수가 지정하는 연결된 서비스 형식에 대한 데이터를 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-165">This cmdlet encrypts data for the linked service type that this parameter specifies.</span></span>
<span data-ttu-id="37a6e-166">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="37a6e-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37a6e-167">OnPremisesSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="37a6e-167">OnPremisesSqlLinkedService</span></span> 
- <span data-ttu-id="37a6e-168">OnPremisesFileSystemLinkedService</span><span class="sxs-lookup"><span data-stu-id="37a6e-168">OnPremisesFileSystemLinkedService</span></span> 
- <span data-ttu-id="37a6e-169">OnPremisesOracleLinkedService</span><span class="sxs-lookup"><span data-stu-id="37a6e-169">OnPremisesOracleLinkedService</span></span> 
- <span data-ttu-id="37a6e-170">OnPremisesOdbcLinkedService</span><span class="sxs-lookup"><span data-stu-id="37a6e-170">OnPremisesOdbcLinkedService</span></span> 
- <span data-ttu-id="37a6e-171">OnPremisesPostgreSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="37a6e-171">OnPremisesPostgreSqlLinkedService</span></span> 
- <span data-ttu-id="37a6e-172">OnPremisesTeradataLinkedService</span><span class="sxs-lookup"><span data-stu-id="37a6e-172">OnPremisesTeradataLinkedService</span></span> 
- <span data-ttu-id="37a6e-173">OnPremisesMySQLLinkedService</span><span class="sxs-lookup"><span data-stu-id="37a6e-173">OnPremisesMySQLLinkedService</span></span> 
- <span data-ttu-id="37a6e-174">OnPremisesDB2LinkedService</span><span class="sxs-lookup"><span data-stu-id="37a6e-174">OnPremisesDB2LinkedService</span></span> 
- <span data-ttu-id="37a6e-175">OnPremisesSybaseLinkedService</span><span class="sxs-lookup"><span data-stu-id="37a6e-175">OnPremisesSybaseLinkedService</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OnPremisesSqlLinkedService, OnPremisesFileSystemLinkedService, OnPremisesOracleLinkedService, OnPremisesOdbcLinkedService, OnPremisesPostgreSqlLinkedService, OnPremisesTeradataLinkedService, OnPremisesMySQLLinkedService, OnPremisesDB2LinkedService, OnPremisesSybaseLinkedService, HdfsLinkedService

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37a6e-176">-Value</span><span class="sxs-lookup"><span data-stu-id="37a6e-176">-Value</span></span>
<span data-ttu-id="37a6e-177">암호화할 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-177">Specifies the value to encrypt.</span></span>
<span data-ttu-id="37a6e-178">연결된 서비스 및 SQL Server Oracle 연결된 서비스의 경우 연결 문자열을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-178">For an on-premises SQL Server linked service and an on-premises Oracle linked service, use a connection string.</span></span>
<span data-ttu-id="37a6e-179">On-premises ODBC 연결된 서비스의 경우 연결 문자열의 자격 증명 부분을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-179">For an on-premises ODBC linked service, use the credential part of the connection string.</span></span>
<span data-ttu-id="37a6e-180">프레미스 파일 시스템 연결된 서비스의 경우 파일 시스템이 게이트웨이 컴퓨터에 로컬인 경우 Local 또는 localhost를 사용하며 파일 시스템이 게이트웨이 컴퓨터와 다른 서버에 있는 경우 서버 \\ \\ 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-180">For on premises file system linked service, if the file system is local to the gateway computer, use Local or localhost, and if the file system is on a server different from the gateway computer, use \\\\servername.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37a6e-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37a6e-181">CommonParameters</span></span>
<span data-ttu-id="37a6e-182">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="37a6e-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37a6e-183">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="37a6e-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37a6e-184">입력</span><span class="sxs-lookup"><span data-stu-id="37a6e-184">INPUTS</span></span>

### <span data-ttu-id="37a6e-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="37a6e-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="37a6e-186">System.String</span><span class="sxs-lookup"><span data-stu-id="37a6e-186">System.String</span></span>

## <span data-ttu-id="37a6e-187">출력</span><span class="sxs-lookup"><span data-stu-id="37a6e-187">OUTPUTS</span></span>

### <span data-ttu-id="37a6e-188">System.String</span><span class="sxs-lookup"><span data-stu-id="37a6e-188">System.String</span></span>

## <span data-ttu-id="37a6e-189">참고 사항</span><span class="sxs-lookup"><span data-stu-id="37a6e-189">NOTES</span></span>
* <span data-ttu-id="37a6e-190">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="37a6e-190">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="37a6e-191">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37a6e-191">RELATED LINKS</span></span>

[<span data-ttu-id="37a6e-192">New-AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="37a6e-192">New-AzDataFactoryEncryptValue</span></span>](./New-AzDataFactoryEncryptValue.md)


