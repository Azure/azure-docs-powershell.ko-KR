---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
ms.openlocfilehash: 8dbb6f79a61d388aec033030de471092fa16ba77
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226065"
---
# <span data-ttu-id="89c9c-101">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="89c9c-101">New-AzStorageShareSASToken</span></span>

## <span data-ttu-id="89c9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="89c9c-103">Azure 저장소 공유에 대 한 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="89c9c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89c9c-104">SYNTAX</span></span>

### <span data-ttu-id="89c9c-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="89c9c-105">SasPolicy</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89c9c-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="89c9c-106">SasPermission</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89c9c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="89c9c-107">DESCRIPTION</span></span>
<span data-ttu-id="89c9c-108">**AzStorageShareSASToken** Cmdlet은 Azure 저장소 공유에 대 한 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-108">The **New-AzStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="89c9c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="89c9c-109">EXAMPLES</span></span>

### <span data-ttu-id="89c9c-110">예제 1: 공유에 대 한 공유 액세스 서명 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="89c9c-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="89c9c-111">이 명령은 ContosoShare 이라는 공유에 대 한 공유 액세스 서명 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="89c9c-112">예제 2: 파이프라인을 사용 하 여 여러 공유 액세스 서명 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="89c9c-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "test" | New-AzStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="89c9c-113">이 명령은 접두사 테스트와 일치 하는 모든 저장소 공유를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="89c9c-114">이 명령은 파이프라인 연산자를 사용 하 여이를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="89c9c-115">현재 cmdlet은 지정 된 사용 권한을 가진 각 저장소 공유에 대 한 공유 액세스 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="89c9c-116">예제 3: 공유 액세스 정책을 사용 하는 공유 액세스 서명 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="89c9c-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="89c9c-117">이 명령은 ContosoPolicy03 이라는 정책이 있는 ContosoShare 이라는 저장소 공유에 대 한 공유 액세스 서명 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="89c9c-118">변수</span><span class="sxs-lookup"><span data-stu-id="89c9c-118">PARAMETERS</span></span>

### <span data-ttu-id="89c9c-119">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="89c9c-119">-Context</span></span>
<span data-ttu-id="89c9c-120">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="89c9c-121">컨텍스트를 가져오려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-121">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89c9c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89c9c-122">-DefaultProfile</span></span>
<span data-ttu-id="89c9c-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89c9c-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="89c9c-124">-ExpiryTime</span></span>
<span data-ttu-id="89c9c-125">공유 액세스 서명이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-125">Specifies the time at which the shared access signature becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89c9c-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="89c9c-126">-FullUri</span></span>
<span data-ttu-id="89c9c-127">이 cmdlet이 full blob URI 및 공유 액세스 서명 토큰을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="89c9c-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="89c9c-128">-IPAddressOrRange</span></span>
<span data-ttu-id="89c9c-129">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="89c9c-130">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="89c9c-131">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="89c9c-131">-Permission</span></span>
<span data-ttu-id="89c9c-132">공유 아래에 있는 공유 및 파일에 액세스할 수 있는 토큰의 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-132">Specifies the permissions in the token to access the share and files under the share.</span></span>
<span data-ttu-id="89c9c-133">이는 문자열 (예: `rwd` 읽기, 쓰기 및 삭제) 이라고 한다는 점에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-133">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89c9c-134">-정책</span><span class="sxs-lookup"><span data-stu-id="89c9c-134">-Policy</span></span>
<span data-ttu-id="89c9c-135">공유에 대 한 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-135">Specifies the stored access policy for a share.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89c9c-136">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="89c9c-136">-Protocol</span></span>
<span data-ttu-id="89c9c-137">요청에 허용 된 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-137">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="89c9c-138">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-138">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="89c9c-139">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="89c9c-139">HttpsOnly</span></span>
* <span data-ttu-id="89c9c-140">HttpsOrHttp의 기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-140">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89c9c-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="89c9c-141">-ShareName</span></span>
<span data-ttu-id="89c9c-142">저장소 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-142">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89c9c-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="89c9c-143">-StartTime</span></span>
<span data-ttu-id="89c9c-144">공유 액세스 서명이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-144">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89c9c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89c9c-145">CommonParameters</span></span>
<span data-ttu-id="89c9c-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89c9c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89c9c-147">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89c9c-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89c9c-148">입력</span><span class="sxs-lookup"><span data-stu-id="89c9c-148">INPUTS</span></span>

### <span data-ttu-id="89c9c-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="89c9c-149">System.String</span></span>

### <span data-ttu-id="89c9c-150">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="89c9c-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="89c9c-151">출력</span><span class="sxs-lookup"><span data-stu-id="89c9c-151">OUTPUTS</span></span>

### <span data-ttu-id="89c9c-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="89c9c-152">System.String</span></span>

## <span data-ttu-id="89c9c-153">상속자</span><span class="sxs-lookup"><span data-stu-id="89c9c-153">NOTES</span></span>
* <span data-ttu-id="89c9c-154">키워드: common, azure, services, data, 저장소, blob, 대기열, 테이블</span><span class="sxs-lookup"><span data-stu-id="89c9c-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="89c9c-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89c9c-155">RELATED LINKS</span></span>

[<span data-ttu-id="89c9c-156">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="89c9c-156">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="89c9c-157">새로운 AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="89c9c-157">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)
