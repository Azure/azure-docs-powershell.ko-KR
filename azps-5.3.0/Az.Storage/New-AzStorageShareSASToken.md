---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
ms.openlocfilehash: 8dbb6f79a61d388aec033030de471092fa16ba77
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494687"
---
# <span data-ttu-id="a5509-101">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="a5509-101">New-AzStorageShareSASToken</span></span>

## <span data-ttu-id="a5509-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5509-102">SYNOPSIS</span></span>
<span data-ttu-id="a5509-103">Azure Storage 공유에 대한 공유 액세스 서명 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="a5509-104">구문</span><span class="sxs-lookup"><span data-stu-id="a5509-104">SYNTAX</span></span>

### <span data-ttu-id="a5509-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="a5509-105">SasPolicy</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5509-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="a5509-106">SasPermission</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5509-107">설명</span><span class="sxs-lookup"><span data-stu-id="a5509-107">DESCRIPTION</span></span>
<span data-ttu-id="a5509-108">**New-AzStorageShareSASToken** cmdlet은 Azure Storage 공유에 대한 공유 액세스 서명 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-108">The **New-AzStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="a5509-109">예제</span><span class="sxs-lookup"><span data-stu-id="a5509-109">EXAMPLES</span></span>

### <span data-ttu-id="a5509-110">예제 1: 공유에 대한 공유 액세스 서명 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="a5509-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="a5509-111">이 명령은 ContosoShare라는 공유에 대한 공유 액세스 서명 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="a5509-112">예제 2: 파이프라인을 사용하여 여러 공유 액세스 서명 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="a5509-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "test" | New-AzStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="a5509-113">이 명령은 사전 테스트와 일치하는 모든 Storage 공유를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="a5509-114">이 명령은 파이프라인 연산자를 사용하여 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a5509-115">현재 cmdlet은 지정된 권한이 있는 각 Storage 공유에 대한 공유 액세스 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="a5509-116">예제 3: 공유 액세스 정책을 사용하는 공유 액세스 서명 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="a5509-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="a5509-117">이 명령은 ContosoPolicy03이라는 정책이 있는 ContosoShare라는 Storage 공유에 대한 공유 액세스 서명 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="a5509-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5509-118">PARAMETERS</span></span>

### <span data-ttu-id="a5509-119">-Context</span><span class="sxs-lookup"><span data-stu-id="a5509-119">-Context</span></span>
<span data-ttu-id="a5509-120">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="a5509-121">컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-121">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a5509-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5509-122">-DefaultProfile</span></span>
<span data-ttu-id="a5509-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5509-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a5509-124">-ExpiryTime</span></span>
<span data-ttu-id="a5509-125">공유 액세스 서명이 유효하지 않은 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-125">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="a5509-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="a5509-126">-FullUri</span></span>
<span data-ttu-id="a5509-127">이 cmdlet이 전체 Blob URI 및 공유 액세스 서명 토큰을 반환하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="a5509-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="a5509-128">-IPAddressOrRange</span></span>
<span data-ttu-id="a5509-129">요청을 수락할 IP 주소 또는 IP 주소 범위를 지정합니다(예: 168.1.5.65 또는 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="a5509-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="a5509-130">범위는 포괄적입니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="a5509-131">-Permission</span><span class="sxs-lookup"><span data-stu-id="a5509-131">-Permission</span></span>
<span data-ttu-id="a5509-132">공유 및 공유 아래에 있는 파일에 액세스하기 위한 토큰의 사용 권한을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-132">Specifies the permissions in the token to access the share and files under the share.</span></span>
<span data-ttu-id="a5509-133">이 문자열은 읽기, 쓰기 및 삭제와 같은 `rwd` 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-133">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="a5509-134">-Policy</span><span class="sxs-lookup"><span data-stu-id="a5509-134">-Policy</span></span>
<span data-ttu-id="a5509-135">공유에 대해 저장된 액세스 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-135">Specifies the stored access policy for a share.</span></span>

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

### <span data-ttu-id="a5509-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="a5509-136">-Protocol</span></span>
<span data-ttu-id="a5509-137">요청에 허용되는 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-137">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="a5509-138">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="a5509-138">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="a5509-139">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="a5509-139">HttpsOnly</span></span>
* <span data-ttu-id="a5509-140">HttpsOrHttp 기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-140">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="a5509-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a5509-141">-ShareName</span></span>
<span data-ttu-id="a5509-142">저장소 공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-142">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="a5509-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a5509-143">-StartTime</span></span>
<span data-ttu-id="a5509-144">공유 액세스 서명이 유효한 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="a5509-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5509-145">CommonParameters</span></span>
<span data-ttu-id="a5509-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a5509-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5509-147">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a5509-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5509-148">입력</span><span class="sxs-lookup"><span data-stu-id="a5509-148">INPUTS</span></span>

### <span data-ttu-id="a5509-149">System.String</span><span class="sxs-lookup"><span data-stu-id="a5509-149">System.String</span></span>

### <span data-ttu-id="a5509-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a5509-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a5509-151">출력</span><span class="sxs-lookup"><span data-stu-id="a5509-151">OUTPUTS</span></span>

### <span data-ttu-id="a5509-152">System.String</span><span class="sxs-lookup"><span data-stu-id="a5509-152">System.String</span></span>

## <span data-ttu-id="a5509-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a5509-153">NOTES</span></span>
* <span data-ttu-id="a5509-154">키워드: 일반, Azure, 서비스, 데이터, 저장소, Blob, 큐, 테이블</span><span class="sxs-lookup"><span data-stu-id="a5509-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="a5509-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5509-155">RELATED LINKS</span></span>

[<span data-ttu-id="a5509-156">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="a5509-156">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="a5509-157">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="a5509-157">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)
