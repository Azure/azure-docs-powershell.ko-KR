---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217168"
---
# <span data-ttu-id="f51d2-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f51d2-101">New-AzStorageContext</span></span>

## <span data-ttu-id="f51d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f51d2-102">SYNOPSIS</span></span>
<span data-ttu-id="f51d2-103">Azure 저장소 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="f51d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f51d2-104">SYNTAX</span></span>

### <span data-ttu-id="f51d2-105">OAuthAccount (기본값)</span><span class="sxs-lookup"><span data-stu-id="f51d2-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="f51d2-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="f51d2-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="f51d2-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="f51d2-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="f51d2-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="f51d2-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f51d2-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="f51d2-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="f51d2-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="f51d2-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="f51d2-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f51d2-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="f51d2-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="f51d2-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="f51d2-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="f51d2-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="f51d2-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="f51d2-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="f51d2-115">설명은</span><span class="sxs-lookup"><span data-stu-id="f51d2-115">DESCRIPTION</span></span>
<span data-ttu-id="f51d2-116">**AzStorageContext** Cmdlet은 Azure 저장소 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>
<span data-ttu-id="f51d2-117">저장소 컨텍스트의 기본 인증은 입력 저장소 계정 이름만을 갖는 경우 OAuth (Azure AD)입니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-117">The default Authentication of a Storage Context is OAuth (Azure AD), if only input Storage account name.</span></span>
<span data-ttu-id="f51d2-118">의 저장소 서비스 인증에 대 한 세부 정보를 참조 https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services 하세요.</span><span class="sxs-lookup"><span data-stu-id="f51d2-118">See details of authentication of the Storage Service in https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services.</span></span>

## <span data-ttu-id="f51d2-119">예제의</span><span class="sxs-lookup"><span data-stu-id="f51d2-119">EXAMPLES</span></span>

### <span data-ttu-id="f51d2-120">예제 1: 저장소 계정 이름 및 키를 지정 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="f51d2-120">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="f51d2-121">이 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-121">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="f51d2-122">예제 2: 연결 문자열을 지정 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="f51d2-122">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="f51d2-123">이 명령은 계정 ContosoGeneral에 대해 지정 된 연결 문자열을 기반으로 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-123">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="f51d2-124">예제 3: 익명 저장소 계정에 대 한 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="f51d2-124">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="f51d2-125">이 명령은 ContosoGeneral 이라는 계정에 대 한 익명 사용을 위한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-125">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="f51d2-126">명령은 HTTP를 연결 프로토콜로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-126">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="f51d2-127">예제 4: 로컬 개발 저장소 계정을 사용 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="f51d2-127">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="f51d2-128">이 명령은 로컬 개발 저장소 계정을 사용 하 여 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-128">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="f51d2-129">명령은 *Local* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-129">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="f51d2-130">예제 5: 로컬 개발자 저장소 계정에 대 한 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="f51d2-130">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="f51d2-131">이 명령은 로컬 개발 저장소 계정을 사용 하 여 컨텍스트를 만든 다음 파이프라인 연산자를 사용 하 여 새 컨텍스트를 **Get-AzStorageContainer** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-131">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f51d2-132">명령은 로컬 개발자 저장소 계정에 대 한 Azure Storage 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-132">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="f51d2-133">예제 6: 여러 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="f51d2-133">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="f51d2-134">첫 번째 명령은 로컬 개발 저장소 계정을 사용 하 여 컨텍스트를 만든 다음 해당 컨텍스트를 $Context 01 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-134">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="f51d2-135">두 번째 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만든 다음 해당 컨텍스트를 $Context 02 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-135">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="f51d2-136">마지막 명령은 **AzStorageContainer** 를 사용 하 여 $Context 01 및 $Context 02에 저장 된 컨텍스트의 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-136">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="f51d2-137">예제 7: 끝점을 사용 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="f51d2-137">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="f51d2-138">이 명령은 지정 된 저장소 끝점을 가진 Azure 저장소 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-138">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="f51d2-139">이 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-139">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="f51d2-140">예제 8: 지정 된 환경을 사용 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="f51d2-140">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="f51d2-141">이 명령은 지정 된 Azure environment가 있는 Azure 저장소 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-141">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="f51d2-142">이 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-142">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="f51d2-143">예제 9: SAS 토큰을 사용 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="f51d2-143">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="f51d2-144">첫 번째 명령은 ContosoMain 이라는 컨테이너에 대 한 **New AzStorageContainerSASToken** cmdlet을 사용 하 여 SAS 토큰을 생성 한 다음 해당 토큰을 $SasToken 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-144">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="f51d2-145">이 토큰은 읽기, 추가, 업데이트 및 삭제 권한에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-145">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="f51d2-146">두 번째 명령은 $SasToken에 저장 된 SAS 토큰을 사용 하는 ContosoGeneral 라는 계정에 대 한 컨텍스트를 만든 다음 해당 컨텍스트를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-146">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="f51d2-147">마지막 명령은 $Context에 저장 된 컨텍스트를 사용 하 여 ContosoMain 이라는 컨테이너와 연결 된 모든 blob을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-147">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="f51d2-148">예제 10: OAuth 인증을 사용 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="f51d2-148">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="f51d2-149">이 명령은 OAuth (Azure AD) 인증을 사용 하 여 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-149">This command creates a context by using the OAuth (Azure AD) Authentication.</span></span>

## <span data-ttu-id="f51d2-150">변수</span><span class="sxs-lookup"><span data-stu-id="f51d2-150">PARAMETERS</span></span>

### <span data-ttu-id="f51d2-151">-익명</span><span class="sxs-lookup"><span data-stu-id="f51d2-151">-Anonymous</span></span>
<span data-ttu-id="f51d2-152">이 cmdlet이 익명 로그온에 대 한 Azure Storage 컨텍스트를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-152">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="f51d2-153">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="f51d2-153">-ConnectionString</span></span>
<span data-ttu-id="f51d2-154">Azure 저장소 컨텍스트에 대 한 연결 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-154">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="f51d2-155">-끝점</span><span class="sxs-lookup"><span data-stu-id="f51d2-155">-Endpoint</span></span>
<span data-ttu-id="f51d2-156">Azure 저장소 컨텍스트에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-156">Specifies the endpoint for the Azure Storage context.</span></span>

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

### <span data-ttu-id="f51d2-157">-환경</span><span class="sxs-lookup"><span data-stu-id="f51d2-157">-Environment</span></span>
<span data-ttu-id="f51d2-158">Azure 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-158">Specifies the Azure environment.</span></span>
<span data-ttu-id="f51d2-159">이 매개 변수에 허용 되는 값은 AzureCloud 및 AzureChinaCloud입니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-159">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="f51d2-160">자세한 내용은을 입력 `Get-Help Get-AzEnvironment` 하세요.</span><span class="sxs-lookup"><span data-stu-id="f51d2-160">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

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

### <span data-ttu-id="f51d2-161">-로컬</span><span class="sxs-lookup"><span data-stu-id="f51d2-161">-Local</span></span>
<span data-ttu-id="f51d2-162">이 cmdlet이 로컬 개발 저장소 계정을 사용 하 여 컨텍스트를 만들기를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-162">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="f51d2-163">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="f51d2-163">-Protocol</span></span>
<span data-ttu-id="f51d2-164">전송 프로토콜 (https/http).</span><span class="sxs-lookup"><span data-stu-id="f51d2-164">Transfer Protocol (https/http).</span></span>

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

### <span data-ttu-id="f51d2-165">-SasToken</span><span class="sxs-lookup"><span data-stu-id="f51d2-165">-SasToken</span></span>
<span data-ttu-id="f51d2-166">컨텍스트에 대 한 SAS (공유 액세스 서명) 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-166">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="f51d2-167">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f51d2-167">-StorageAccountKey</span></span>
<span data-ttu-id="f51d2-168">Azure 저장소 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-168">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="f51d2-169">이 cmdlet은이 매개 변수에서 지정 하는 키에 대 한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-169">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="f51d2-170">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f51d2-170">-StorageAccountName</span></span>
<span data-ttu-id="f51d2-171">Azure 저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-171">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="f51d2-172">이 cmdlet은이 매개 변수에서 지정 하는 계정에 대 한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-172">This cmdlet creates a context for the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="f51d2-173">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="f51d2-173">-UseConnectedAccount</span></span>
<span data-ttu-id="f51d2-174">이 cmdlet이 OAuth (Azure AD) 인증을 사용 하 여 Azure Storage 컨텍스트를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-174">Indicates that this cmdlet creates an Azure Storage context with OAuth (Azure AD) Authentication.</span></span>
<span data-ttu-id="f51d2-175">다른 인증을 지정 하지 않은 경우 cmdlet이 기본적으로 OAuth 인증을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-175">The cmdlet will use OAuth Authentication by default, when other authentication not specified.</span></span>

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

### <span data-ttu-id="f51d2-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f51d2-176">CommonParameters</span></span>
<span data-ttu-id="f51d2-177">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f51d2-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f51d2-178">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f51d2-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f51d2-179">입력</span><span class="sxs-lookup"><span data-stu-id="f51d2-179">INPUTS</span></span>

### <span data-ttu-id="f51d2-180">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f51d2-180">System.String</span></span>

## <span data-ttu-id="f51d2-181">출력</span><span class="sxs-lookup"><span data-stu-id="f51d2-181">OUTPUTS</span></span>

### <span data-ttu-id="f51d2-182">WindowsAzure.-저장소. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f51d2-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="f51d2-183">상속자</span><span class="sxs-lookup"><span data-stu-id="f51d2-183">NOTES</span></span>

## <span data-ttu-id="f51d2-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f51d2-184">RELATED LINKS</span></span>

[<span data-ttu-id="f51d2-185">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="f51d2-185">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="f51d2-186">새로운 AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="f51d2-186">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


