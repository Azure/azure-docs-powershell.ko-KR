---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349454"
---
# <span data-ttu-id="d6812-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d6812-101">New-AzStorageContext</span></span>

## <span data-ttu-id="d6812-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6812-102">SYNOPSIS</span></span>
<span data-ttu-id="d6812-103">Azure Storage 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="d6812-104">구문</span><span class="sxs-lookup"><span data-stu-id="d6812-104">SYNTAX</span></span>

### <span data-ttu-id="d6812-105">OAuthAccount(기본값)</span><span class="sxs-lookup"><span data-stu-id="d6812-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="d6812-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="d6812-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="d6812-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="d6812-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="d6812-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="d6812-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6812-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="d6812-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="d6812-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="d6812-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="d6812-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d6812-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="d6812-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="d6812-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="d6812-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d6812-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="d6812-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="d6812-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="d6812-115">설명</span><span class="sxs-lookup"><span data-stu-id="d6812-115">DESCRIPTION</span></span>
<span data-ttu-id="d6812-116">**New-AzStorageContext** cmdlet은 Azure Storage 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>
<span data-ttu-id="d6812-117">스토리지 계정 이름을 입력하는 경우 스토리지 컨텍스트의 기본 인증은 OAuth(Azure AD)입니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-117">The default Authentication of a Storage Context is OAuth (Azure AD), if only input Storage account name.</span></span>
<span data-ttu-id="d6812-118">에서 Storage 서비스의 인증에 대한 세부 정보를 https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-118">See details of authentication of the Storage Service in https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services.</span></span>

## <span data-ttu-id="d6812-119">예제</span><span class="sxs-lookup"><span data-stu-id="d6812-119">EXAMPLES</span></span>

### <span data-ttu-id="d6812-120">예제 1: 저장소 계정 이름 및 키를 지정하여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="d6812-120">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="d6812-121">이 명령은 지정된 키를 사용하는 ContosoGeneral이라는 계정에 대한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-121">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="d6812-122">예제 2: 연결 문자열을 지정하여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="d6812-122">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="d6812-123">이 명령은 ContosoGeneral 계정에 대해 지정된 연결 문자열을 기반으로 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-123">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="d6812-124">예제 3: 익명 저장소 계정에 대한 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="d6812-124">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="d6812-125">이 명령은 ContosoGeneral이라는 계정에 익명으로 사용하기 위한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-125">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="d6812-126">이 명령은 HTTP를 연결 프로토콜로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-126">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="d6812-127">예제 4: 로컬 개발 저장소 계정을 사용하여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="d6812-127">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="d6812-128">이 명령은 로컬 개발 저장소 계정을 사용하여 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-128">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="d6812-129">이 명령은 Local 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="d6812-129">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="d6812-130">예제 5: 로컬 개발자 저장소 계정에 대한 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-130">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="d6812-131">이 명령은 로컬 개발 저장소 계정을 사용하여 컨텍스트를 만든 다음 파이프라인 연산자를 사용하여 **Get-AzStorageContainer** cmdlet에 새 컨텍스트를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-131">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d6812-132">이 명령은 로컬 개발자 스토리지 계정에 대한 Azure Storage 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-132">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="d6812-133">예제 6: 여러 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-133">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="d6812-134">첫 번째 명령은 로컬 개발 저장소 계정을 사용하여 컨텍스트를 만든 다음 해당 컨텍스트를 $Context 01 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-134">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="d6812-135">두 번째 명령은 지정된 키를 사용하는 ContosoGeneral이라는 계정에 대한 컨텍스트를 만든 다음 해당 컨텍스트를 $Context 02 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-135">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="d6812-136">마지막 명령은 **Get-AzStorageContainer를** 사용하여 $Context 01 및 $Context 02에 저장된 컨텍스트에 대한 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-136">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="d6812-137">예제 7: 엔드포인트를 사용하여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="d6812-137">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="d6812-138">이 명령은 지정된 스토리지 엔드포인트가 있는 Azure Storage 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-138">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="d6812-139">이 명령은 지정된 키를 사용하는 ContosoGeneral이라는 계정에 대한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-139">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="d6812-140">예제 8: 지정된 환경을 사용하여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="d6812-140">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="d6812-141">이 명령은 지정된 Azure 환경이 있는 Azure 저장소 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-141">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="d6812-142">이 명령은 지정된 키를 사용하는 ContosoGeneral이라는 계정에 대한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-142">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="d6812-143">예제 9: SAS 토큰을 사용하여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="d6812-143">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="d6812-144">첫 번째 명령은 ContosoMain이라는 컨테이너에 **New-AzStorageContainerSASToken** cmdlet을 사용하여 SAS 토큰을 생성한 다음, 해당 토큰을 $SasToken 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-144">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="d6812-145">해당 토큰은 읽기, 추가, 업데이트 및 삭제 권한을 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-145">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="d6812-146">두 번째 명령은 ContosoGeneral이라는 계정에 대한 컨텍스트를 만들고, 이 계정에 저장된 SAS 토큰을 $SasToken 해당 컨텍스트를 $Context 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-146">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="d6812-147">마지막 명령은 컨테이너에 저장된 컨텍스트를 사용하여 ContosoMain이라는 컨테이너와 연결된 모든 blob을 $Context.</span><span class="sxs-lookup"><span data-stu-id="d6812-147">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="d6812-148">예제 10: OAuth 인증을 사용하여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="d6812-148">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="d6812-149">이 명령은 OAuth(Azure AD) 인증을 사용하여 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-149">This command creates a context by using the OAuth (Azure AD) Authentication.</span></span>

## <span data-ttu-id="d6812-150">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6812-150">PARAMETERS</span></span>

### <span data-ttu-id="d6812-151">-Anonymous</span><span class="sxs-lookup"><span data-stu-id="d6812-151">-Anonymous</span></span>
<span data-ttu-id="d6812-152">이 cmdlet이 익명 로그온에 대한 Azure Storage 컨텍스트를 만들었다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-152">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6812-153">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d6812-153">-ConnectionString</span></span>
<span data-ttu-id="d6812-154">Azure Storage 컨텍스트에 대한 연결 문자열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-154">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6812-155">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="d6812-155">-Endpoint</span></span>
<span data-ttu-id="d6812-156">Azure Storage 컨텍스트에 대한 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-156">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6812-157">-Environment</span><span class="sxs-lookup"><span data-stu-id="d6812-157">-Environment</span></span>
<span data-ttu-id="d6812-158">Azure 환경을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-158">Specifies the Azure environment.</span></span>
<span data-ttu-id="d6812-159">이 매개 변수에 허용되는 값은 AzureCloud 및 AzureChinaCloud입니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-159">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="d6812-160">자세한 내용은 `Get-Help Get-AzEnvironment` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-160">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6812-161">-Local</span><span class="sxs-lookup"><span data-stu-id="d6812-161">-Local</span></span>
<span data-ttu-id="d6812-162">이 cmdlet이 로컬 개발 저장소 계정을 사용하여 컨텍스트를 만드는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-162">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6812-163">-Protocol</span><span class="sxs-lookup"><span data-stu-id="d6812-163">-Protocol</span></span>
<span data-ttu-id="d6812-164">전송 프로토콜(https/http).</span><span class="sxs-lookup"><span data-stu-id="d6812-164">Transfer Protocol (https/http).</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6812-165">-SasToken</span><span class="sxs-lookup"><span data-stu-id="d6812-165">-SasToken</span></span>
<span data-ttu-id="d6812-166">컨텍스트에 대한 SAS(공유 액세스 서명) 토큰을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-166">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6812-167">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d6812-167">-StorageAccountKey</span></span>
<span data-ttu-id="d6812-168">Azure Storage 계정 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-168">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="d6812-169">이 cmdlet은 이 매개 변수가 지정하는 키에 대한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-169">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6812-170">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d6812-170">-StorageAccountName</span></span>
<span data-ttu-id="d6812-171">Azure Storage 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-171">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="d6812-172">이 cmdlet은 이 매개 변수가 지정하는 계정에 대한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-172">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6812-173">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="d6812-173">-UseConnectedAccount</span></span>
<span data-ttu-id="d6812-174">이 cmdlet이 OAuth(Azure AD) 인증을 사용하여 Azure Storage 컨텍스트를 만들었다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-174">Indicates that this cmdlet creates an Azure Storage context with OAuth (Azure AD) Authentication.</span></span>
<span data-ttu-id="d6812-175">다른 인증이 지정되지 않은 경우 cmdlet은 기본적으로 OAuth 인증을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-175">The cmdlet will use OAuth Authentication by default, when other authentication not specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6812-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6812-176">CommonParameters</span></span>
<span data-ttu-id="d6812-177">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d6812-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6812-178">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d6812-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6812-179">입력</span><span class="sxs-lookup"><span data-stu-id="d6812-179">INPUTS</span></span>

### <span data-ttu-id="d6812-180">System.String</span><span class="sxs-lookup"><span data-stu-id="d6812-180">System.String</span></span>

## <span data-ttu-id="d6812-181">출력</span><span class="sxs-lookup"><span data-stu-id="d6812-181">OUTPUTS</span></span>

### <span data-ttu-id="d6812-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d6812-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="d6812-183">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d6812-183">NOTES</span></span>

## <span data-ttu-id="d6812-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6812-184">RELATED LINKS</span></span>

[<span data-ttu-id="d6812-185">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d6812-185">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="d6812-186">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="d6812-186">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


