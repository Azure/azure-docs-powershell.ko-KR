---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4db0b752e8bf887e899a4de6a8e4175eaa2d9855
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523676"
---
# <span data-ttu-id="69b1a-101">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="69b1a-101">New-AzureStorageContext</span></span>

## <span data-ttu-id="69b1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="69b1a-103">Azure 저장소 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="69b1a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69b1a-104">SYNTAX</span></span>

### <span data-ttu-id="69b1a-105">AccountNameAndKey (기본값)</span><span class="sxs-lookup"><span data-stu-id="69b1a-105">AccountNameAndKey (Default)</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="69b1a-106">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="69b1a-106">AccountNameAndKeyEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="69b1a-107">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="69b1a-107">AnonymousAccount</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="69b1a-108">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="69b1a-108">AnonymousAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="69b1a-109">SasToken</span><span class="sxs-lookup"><span data-stu-id="69b1a-109">SasToken</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="69b1a-110">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="69b1a-110">SasTokenWithAzureEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="69b1a-111">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="69b1a-111">ConnectionString</span></span>
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="69b1a-112">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="69b1a-112">LocalDevelopment</span></span>
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="69b1a-113">설명은</span><span class="sxs-lookup"><span data-stu-id="69b1a-113">DESCRIPTION</span></span>
<span data-ttu-id="69b1a-114">**새-AzureStorageContext** Cmdlet은 Azure 저장소 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-114">The **New-AzureStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="69b1a-115">예제의</span><span class="sxs-lookup"><span data-stu-id="69b1a-115">EXAMPLES</span></span>

### <span data-ttu-id="69b1a-116">예제 1: 저장소 계정 이름 및 키를 지정 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="69b1a-116">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="69b1a-117">이 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-117">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="69b1a-118">예제 2: 연결 문자열을 지정 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="69b1a-118">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="69b1a-119">이 명령은 계정 ContosoGeneral에 대해 지정 된 연결 문자열을 기반으로 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-119">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="69b1a-120">예제 3: 익명 저장소 계정에 대 한 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="69b1a-120">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="69b1a-121">이 명령은 ContosoGeneral 이라는 계정에 대 한 익명 사용을 위한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-121">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="69b1a-122">명령은 HTTP를 연결 프로토콜로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-122">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="69b1a-123">예제 4: 로컬 개발 저장소 계정을 사용 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="69b1a-123">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local
```

<span data-ttu-id="69b1a-124">이 명령은 로컬 개발 저장소 계정을 사용 하 여 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-124">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="69b1a-125">명령은 *Local* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-125">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="69b1a-126">예제 5: 로컬 개발자 저장소 계정에 대 한 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="69b1a-126">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

<span data-ttu-id="69b1a-127">이 명령은 로컬 개발 저장소 계정을 사용 하 여 컨텍스트를 만든 다음 파이프라인 연산자를 사용 하 여 새 컨텍스트를 **Get-AzureStorageContainer** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-127">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzureStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="69b1a-128">명령은 로컬 개발자 저장소 계정에 대 한 Azure Storage 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-128">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="69b1a-129">예제 6: 여러 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="69b1a-129">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

<span data-ttu-id="69b1a-130">첫 번째 명령은 로컬 개발 저장소 계정을 사용 하 여 컨텍스트를 만든 다음 해당 컨텍스트를 $Context 01 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-130">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>

<span data-ttu-id="69b1a-131">두 번째 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만든 다음 해당 컨텍스트를 $Context 02 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-131">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>

<span data-ttu-id="69b1a-132">마지막 명령은 **AzureStorageContainer** 를 사용 하 여 $Context 01 및 $Context 02에 저장 된 컨텍스트의 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-132">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="69b1a-133">예제 7: 끝점을 사용 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="69b1a-133">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="69b1a-134">이 명령은 지정 된 저장소 끝점을 가진 Azure 저장소 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-134">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="69b1a-135">이 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-135">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="69b1a-136">예제 8: 지정 된 환경을 사용 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="69b1a-136">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="69b1a-137">이 명령은 지정 된 Azure environment가 있는 Azure 저장소 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-137">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="69b1a-138">이 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-138">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="69b1a-139">예제 9: SAS 토큰을 사용 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="69b1a-139">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "raud"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="69b1a-140">첫 번째 명령은 ContosoMain 이라는 컨테이너에 대 한 **New AzureStorageContainerSASToken** cmdlet을 사용 하 여 SAS 토큰을 생성 한 다음 해당 토큰을 $SasToken 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-140">The first command generates an SAS token by using the **New-AzureStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="69b1a-141">이 토큰은 읽기, 추가, 업데이트 및 삭제 권한에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-141">That token is for read, add, update, and delete permissions.</span></span>

<span data-ttu-id="69b1a-142">두 번째 명령은 $SasToken에 저장 된 SAS 토큰을 사용 하는 ContosoGeneral 라는 계정에 대 한 컨텍스트를 만든 다음 해당 컨텍스트를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-142">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>

<span data-ttu-id="69b1a-143">마지막 명령은 $Context에 저장 된 컨텍스트를 사용 하 여 ContosoMain 이라는 컨테이너와 연결 된 모든 blob을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-143">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

## <span data-ttu-id="69b1a-144">변수</span><span class="sxs-lookup"><span data-stu-id="69b1a-144">PARAMETERS</span></span>

### <span data-ttu-id="69b1a-145">-익명</span><span class="sxs-lookup"><span data-stu-id="69b1a-145">-Anonymous</span></span>
<span data-ttu-id="69b1a-146">이 cmdlet이 익명 로그온에 대 한 Azure Storage 컨텍스트를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-146">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b1a-147">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="69b1a-147">-ConnectionString</span></span>
<span data-ttu-id="69b1a-148">Azure 저장소 컨텍스트에 대 한 연결 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-148">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: String
Parameter Sets: ConnectionString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b1a-149">-끝점</span><span class="sxs-lookup"><span data-stu-id="69b1a-149">-Endpoint</span></span>
<span data-ttu-id="69b1a-150">Azure 저장소 컨텍스트에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-150">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b1a-151">-환경</span><span class="sxs-lookup"><span data-stu-id="69b1a-151">-Environment</span></span>
<span data-ttu-id="69b1a-152">Azure 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-152">Specifies the Azure environment.</span></span>
<span data-ttu-id="69b1a-153">이 매개 변수에 허용 되는 값은 AzureCloud 및 AzureChinaCloud입니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-153">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="69b1a-154">자세한 내용은을 입력 `Get-Help Get-AzureEnvironment` 하세요.</span><span class="sxs-lookup"><span data-stu-id="69b1a-154">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SasTokenWithAzureEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69b1a-155">-로컬</span><span class="sxs-lookup"><span data-stu-id="69b1a-155">-Local</span></span>
<span data-ttu-id="69b1a-156">이 cmdlet이 로컬 개발 저장소 계정을 사용 하 여 컨텍스트를 만들기를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-156">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LocalDevelopment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b1a-157">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="69b1a-157">-Protocol</span></span>
<span data-ttu-id="69b1a-158">계정 SA로 작성 된 요청에 허용 되는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-158">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="69b1a-159">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="69b1a-160">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="69b1a-160">HttpsOnly</span></span>
- <span data-ttu-id="69b1a-161">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="69b1a-161">HttpsOrHttp</span></span>

<span data-ttu-id="69b1a-162">기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-162">The default value is HttpsOrHttp.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
Aliases: 
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b1a-163">-SasToken</span><span class="sxs-lookup"><span data-stu-id="69b1a-163">-SasToken</span></span>
<span data-ttu-id="69b1a-164">컨텍스트에 대 한 SAS (공유 액세스 서명) 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-164">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b1a-165">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="69b1a-165">-StorageAccountKey</span></span>
<span data-ttu-id="69b1a-166">Azure 저장소 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-166">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="69b1a-167">이 cmdlet은이 매개 변수에서 지정 하는 키에 대 한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-167">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b1a-168">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="69b1a-168">-StorageAccountName</span></span>
<span data-ttu-id="69b1a-169">Azure 저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-169">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="69b1a-170">이 cmdlet은이 매개 변수에서 지정 하는 계정에 대 한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-170">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b1a-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69b1a-171">CommonParameters</span></span>
<span data-ttu-id="69b1a-172">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b1a-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69b1a-173">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69b1a-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69b1a-174">입력</span><span class="sxs-lookup"><span data-stu-id="69b1a-174">INPUTS</span></span>

## <span data-ttu-id="69b1a-175">출력</span><span class="sxs-lookup"><span data-stu-id="69b1a-175">OUTPUTS</span></span>

### <span data-ttu-id="69b1a-176">AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="69b1a-176">AzureStorageContext</span></span>

## <span data-ttu-id="69b1a-177">상속자</span><span class="sxs-lookup"><span data-stu-id="69b1a-177">NOTES</span></span>

## <span data-ttu-id="69b1a-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69b1a-178">RELATED LINKS</span></span>

[<span data-ttu-id="69b1a-179">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="69b1a-179">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="69b1a-180">새로운 AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="69b1a-180">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)


