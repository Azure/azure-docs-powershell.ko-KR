---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: eb84c4c00e54d06588a82f10bad824737e8546f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874240"
---
# <span data-ttu-id="6e38a-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="6e38a-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="6e38a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e38a-102">SYNOPSIS</span></span>
<span data-ttu-id="6e38a-103">Azure 저장소 컨테이너에 대 한 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="6e38a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e38a-104">SYNTAX</span></span>

### <span data-ttu-id="6e38a-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="6e38a-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e38a-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="6e38a-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e38a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6e38a-107">DESCRIPTION</span></span>
<span data-ttu-id="6e38a-108">**AzStorageContainerSASToken** Cmdlet은 Azure 저장소 컨테이너에 대 한 SAS (공유 액세스 서명) 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="6e38a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6e38a-109">EXAMPLES</span></span>

### <span data-ttu-id="6e38a-110">예제 1: 전체 컨테이너 권한을 사용 하 여 컨테이너 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="6e38a-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="6e38a-111">이 예제에서는 모든 컨테이너 권한이 있는 컨테이너 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="6e38a-112">예제 2: 파이프라인을 통해 다중 컨테이너 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="6e38a-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="6e38a-113">이 예제에서는 파이프라인을 사용 하 여 컨테이너 SAS 토큰을 여러 개 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="6e38a-114">예제 3: 공유 액세스 정책을 사용 하 여 컨테이너 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="6e38a-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="6e38a-115">이 예제에서는 공유 액세스 정책을 사용 하 여 컨테이너 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="6e38a-116">변수</span><span class="sxs-lookup"><span data-stu-id="6e38a-116">PARAMETERS</span></span>

### <span data-ttu-id="6e38a-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="6e38a-117">-Context</span></span>
<span data-ttu-id="6e38a-118">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6e38a-119">New-AzStorageContext cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-119">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6e38a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e38a-120">-DefaultProfile</span></span>
<span data-ttu-id="6e38a-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e38a-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6e38a-122">-ExpiryTime</span></span>
<span data-ttu-id="6e38a-123">공유 액세스 서명이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-123">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="6e38a-124">사용자가 시작 시간을 설정 했지만 만료 시간이 아닌 경우 만료 시간은 시작 시간에 1 시간을 더한 값으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-124">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="6e38a-125">시작 시간이 나 만료 시간이 모두 지정 되어 있지 않은 경우 만료 시간은 현재 시간에 1 시간을 더한 값으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-125">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="6e38a-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="6e38a-126">-FullUri</span></span>
<span data-ttu-id="6e38a-127">이 cmdlet이 full blob URI 및 공유 액세스 서명 토큰을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="6e38a-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="6e38a-128">-IPAddressOrRange</span></span>
<span data-ttu-id="6e38a-129">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="6e38a-130">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="6e38a-131">-이름</span><span class="sxs-lookup"><span data-stu-id="6e38a-131">-Name</span></span>
<span data-ttu-id="6e38a-132">Azure 저장소 컨테이너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-132">Specifies an Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e38a-133">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="6e38a-133">-Permission</span></span>
<span data-ttu-id="6e38a-134">저장소 컨테이너에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-134">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="6e38a-135">이는 문자열 (예: `rwd` 읽기, 쓰기 및 삭제) 이라고 한다는 점에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-135">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="6e38a-136">-정책</span><span class="sxs-lookup"><span data-stu-id="6e38a-136">-Policy</span></span>
<span data-ttu-id="6e38a-137">Azure 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-137">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="6e38a-138">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="6e38a-138">-Protocol</span></span>
<span data-ttu-id="6e38a-139">요청에 허용 된 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-139">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="6e38a-140">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-140">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="6e38a-141">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="6e38a-141">HttpsOnly</span></span>
* <span data-ttu-id="6e38a-142">HttpsOrHttp의 기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-142">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="6e38a-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6e38a-143">-StartTime</span></span>
<span data-ttu-id="6e38a-144">공유 액세스 서명이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="6e38a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e38a-145">CommonParameters</span></span>
<span data-ttu-id="6e38a-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e38a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e38a-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e38a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e38a-148">입력</span><span class="sxs-lookup"><span data-stu-id="6e38a-148">INPUTS</span></span>

### <span data-ttu-id="6e38a-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6e38a-149">System.String</span></span>

### <span data-ttu-id="6e38a-150">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e38a-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6e38a-151">출력</span><span class="sxs-lookup"><span data-stu-id="6e38a-151">OUTPUTS</span></span>

### <span data-ttu-id="6e38a-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6e38a-152">System.String</span></span>

## <span data-ttu-id="6e38a-153">상속자</span><span class="sxs-lookup"><span data-stu-id="6e38a-153">NOTES</span></span>

## <span data-ttu-id="6e38a-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e38a-154">RELATED LINKS</span></span>

[<span data-ttu-id="6e38a-155">새로운 AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6e38a-155">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)
