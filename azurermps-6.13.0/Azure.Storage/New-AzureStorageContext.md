---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
ms.openlocfilehash: 9de6b2b52205bdf80de9c57e3e338f4b7216c5ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531555"
---
# <span data-ttu-id="a1610-101">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a1610-101">New-AzureStorageContext</span></span>

## <span data-ttu-id="a1610-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1610-102">SYNOPSIS</span></span>
<span data-ttu-id="a1610-103">Azure 저장소 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-103">Creates an Azure Storage context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1610-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a1610-104">SYNTAX</span></span>

### <span data-ttu-id="a1610-105">OAuthAccount (기본값)</span><span class="sxs-lookup"><span data-stu-id="a1610-105">OAuthAccount (Default)</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="a1610-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="a1610-106">AccountNameAndKey</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="a1610-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="a1610-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="a1610-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="a1610-108">AnonymousAccount</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1610-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="a1610-109">AnonymousAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="a1610-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="a1610-110">SasToken</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="a1610-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a1610-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="a1610-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="a1610-112">OAuthAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="a1610-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a1610-113">ConnectionString</span></span>
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="a1610-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="a1610-114">LocalDevelopment</span></span>
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="a1610-115">설명은</span><span class="sxs-lookup"><span data-stu-id="a1610-115">DESCRIPTION</span></span>
<span data-ttu-id="a1610-116">**새-AzureStorageContext** Cmdlet은 Azure 저장소 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-116">The **New-AzureStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="a1610-117">예제의</span><span class="sxs-lookup"><span data-stu-id="a1610-117">EXAMPLES</span></span>

### <span data-ttu-id="a1610-118">예제 1: 저장소 계정 이름 및 키를 지정 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="a1610-118">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="a1610-119">이 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-119">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="a1610-120">예제 2: 연결 문자열을 지정 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="a1610-120">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="a1610-121">이 명령은 계정 ContosoGeneral에 대해 지정 된 연결 문자열을 기반으로 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-121">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="a1610-122">예제 3: 익명 저장소 계정에 대 한 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="a1610-122">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="a1610-123">이 명령은 ContosoGeneral 이라는 계정에 대 한 익명 사용을 위한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-123">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="a1610-124">명령은 HTTP를 연결 프로토콜로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-124">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="a1610-125">예제 4: 로컬 개발 저장소 계정을 사용 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="a1610-125">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local
```

<span data-ttu-id="a1610-126">이 명령은 로컬 개발 저장소 계정을 사용 하 여 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-126">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="a1610-127">명령은 *Local* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-127">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="a1610-128">예제 5: 로컬 개발자 저장소 계정에 대 한 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="a1610-128">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

<span data-ttu-id="a1610-129">이 명령은 로컬 개발 저장소 계정을 사용 하 여 컨텍스트를 만든 다음 파이프라인 연산자를 사용 하 여 새 컨텍스트를 **Get-AzureStorageContainer** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-129">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzureStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a1610-130">명령은 로컬 개발자 저장소 계정에 대 한 Azure Storage 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-130">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="a1610-131">예제 6: 여러 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="a1610-131">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

<span data-ttu-id="a1610-132">첫 번째 명령은 로컬 개발 저장소 계정을 사용 하 여 컨텍스트를 만든 다음 해당 컨텍스트를 $Context 01 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-132">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="a1610-133">두 번째 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만든 다음 해당 컨텍스트를 $Context 02 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-133">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="a1610-134">마지막 명령은 **AzureStorageContainer** 를 사용 하 여 $Context 01 및 $Context 02에 저장 된 컨텍스트의 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-134">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="a1610-135">예제 7: 끝점을 사용 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="a1610-135">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="a1610-136">이 명령은 지정 된 저장소 끝점을 가진 Azure 저장소 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-136">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="a1610-137">이 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-137">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="a1610-138">예제 8: 지정 된 환경을 사용 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="a1610-138">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="a1610-139">이 명령은 지정 된 Azure environment가 있는 Azure 저장소 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-139">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="a1610-140">이 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-140">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="a1610-141">예제 9: SAS 토큰을 사용 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="a1610-141">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="a1610-142">첫 번째 명령은 ContosoMain 이라는 컨테이너에 대 한 **New AzureStorageContainerSASToken** cmdlet을 사용 하 여 SAS 토큰을 생성 한 다음 해당 토큰을 $SasToken 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-142">The first command generates an SAS token by using the **New-AzureStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="a1610-143">이 토큰은 읽기, 추가, 업데이트 및 삭제 권한에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-143">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="a1610-144">두 번째 명령은 $SasToken에 저장 된 SAS 토큰을 사용 하는 ContosoGeneral 라는 계정에 대 한 컨텍스트를 만든 다음 해당 컨텍스트를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-144">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="a1610-145">마지막 명령은 $Context에 저장 된 컨텍스트를 사용 하 여 ContosoMain 이라는 컨테이너와 연결 된 모든 blob을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-145">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="a1610-146">예제 10: OAuth 인증을 사용 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="a1610-146">Example 10: Create a context by using the OAuth Authentication</span></span>
```
C:\PS>Connect-AzureRmAccount
C:\PS> $Context = New-AzureStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="a1610-147">이 명령은 OAuth 인증을 사용 하 여 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-147">This command creates a context by using the OAuth Authentication.</span></span>

## <span data-ttu-id="a1610-148">변수</span><span class="sxs-lookup"><span data-stu-id="a1610-148">PARAMETERS</span></span>

### <span data-ttu-id="a1610-149">-익명</span><span class="sxs-lookup"><span data-stu-id="a1610-149">-Anonymous</span></span>
<span data-ttu-id="a1610-150">이 cmdlet이 익명 로그온에 대 한 Azure Storage 컨텍스트를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-150">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="a1610-151">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a1610-151">-ConnectionString</span></span>
<span data-ttu-id="a1610-152">Azure 저장소 컨텍스트에 대 한 연결 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-152">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="a1610-153">-끝점</span><span class="sxs-lookup"><span data-stu-id="a1610-153">-Endpoint</span></span>
<span data-ttu-id="a1610-154">Azure 저장소 컨텍스트에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-154">Specifies the endpoint for the Azure Storage context.</span></span>

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

### <span data-ttu-id="a1610-155">-환경</span><span class="sxs-lookup"><span data-stu-id="a1610-155">-Environment</span></span>
<span data-ttu-id="a1610-156">Azure 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-156">Specifies the Azure environment.</span></span>
<span data-ttu-id="a1610-157">이 매개 변수에 허용 되는 값은 AzureCloud 및 AzureChinaCloud입니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-157">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="a1610-158">자세한 내용은을 입력 `Get-Help Get-AzureEnvironment` 하세요.</span><span class="sxs-lookup"><span data-stu-id="a1610-158">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

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

### <span data-ttu-id="a1610-159">-로컬</span><span class="sxs-lookup"><span data-stu-id="a1610-159">-Local</span></span>
<span data-ttu-id="a1610-160">이 cmdlet이 로컬 개발 저장소 계정을 사용 하 여 컨텍스트를 만들기를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-160">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="a1610-161">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="a1610-161">-Protocol</span></span>
<span data-ttu-id="a1610-162">전송 프로토콜 (https/http).</span><span class="sxs-lookup"><span data-stu-id="a1610-162">Transfer Protocol (https/http).</span></span>

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

### <span data-ttu-id="a1610-163">-SasToken</span><span class="sxs-lookup"><span data-stu-id="a1610-163">-SasToken</span></span>
<span data-ttu-id="a1610-164">컨텍스트에 대 한 SAS (공유 액세스 서명) 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-164">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="a1610-165">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a1610-165">-StorageAccountKey</span></span>
<span data-ttu-id="a1610-166">Azure 저장소 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-166">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="a1610-167">이 cmdlet은이 매개 변수에서 지정 하는 키에 대 한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-167">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="a1610-168">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a1610-168">-StorageAccountName</span></span>
<span data-ttu-id="a1610-169">Azure 저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-169">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="a1610-170">이 cmdlet은이 매개 변수에서 지정 하는 계정에 대 한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-170">This cmdlet creates a context for the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="a1610-171">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="a1610-171">-UseConnectedAccount</span></span>
<span data-ttu-id="a1610-172">이 cmdlet이 OAuth 인증을 사용 하 여 Azure Storage 컨텍스트를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-172">Indicates that this cmdlet creates an Azure Storage context with OAuth Authentication.</span></span>
<span data-ttu-id="a1610-173">다른 anthentication가 지정 되지 않은 경우 cmdlet은 기본적으로 OAuth 인증을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-173">The cmdlet will use OAuth Authentication by default, when other anthentication not specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1610-174">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="a1610-174">-UseConnectedAccount</span></span>
<span data-ttu-id="a1610-175">이 cmdlet이 OAuth 인증을 사용 하 여 Azure Storage 컨텍스트를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-175">Indicates that this cmdlet creates an Azure Storage context with OAuth Authentication.</span></span>
<span data-ttu-id="a1610-176">다른 anthentication가 지정 되지 않은 경우 cmdlet은 기본적으로 OAuth 인증을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-176">The cmdlet will use OAuth Authentication by default, when other anthentication not specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1610-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1610-177">CommonParameters</span></span>
<span data-ttu-id="a1610-178">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1610-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1610-179">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1610-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1610-180">입력</span><span class="sxs-lookup"><span data-stu-id="a1610-180">INPUTS</span></span>

### <span data-ttu-id="a1610-181">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a1610-181">System.String</span></span>

## <span data-ttu-id="a1610-182">출력</span><span class="sxs-lookup"><span data-stu-id="a1610-182">OUTPUTS</span></span>

### <span data-ttu-id="a1610-183">WindowsAzure.-저장소. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a1610-183">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="a1610-184">상속자</span><span class="sxs-lookup"><span data-stu-id="a1610-184">NOTES</span></span>

## <span data-ttu-id="a1610-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1610-185">RELATED LINKS</span></span>

[<span data-ttu-id="a1610-186">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a1610-186">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="a1610-187">새로운 AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="a1610-187">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)


