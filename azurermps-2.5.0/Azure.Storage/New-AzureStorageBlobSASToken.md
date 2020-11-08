---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageblobsastoken
schema: 2.0.0
ms.openlocfilehash: a85f9a741848824554bb3df49075fad49bfe4015
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882065"
---
# <span data-ttu-id="9485e-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="9485e-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="9485e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9485e-102">SYNOPSIS</span></span>
<span data-ttu-id="9485e-103">Azure 저장소 blob에 대 한 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-103">Generates a SAS token for an Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9485e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9485e-104">SYNTAX</span></span>

### <span data-ttu-id="9485e-105">BlobNameWithPermission (기본값)</span><span class="sxs-lookup"><span data-stu-id="9485e-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9485e-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="9485e-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9485e-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="9485e-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9485e-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="9485e-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9485e-109">설명은</span><span class="sxs-lookup"><span data-stu-id="9485e-109">DESCRIPTION</span></span>
<span data-ttu-id="9485e-110">**AzureStorageBlobSASToken** Cmdlet은 Azure storage blob에 대 한 SAS (공유 액세스 서명) 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="9485e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9485e-111">EXAMPLES</span></span>

### <span data-ttu-id="9485e-112">예제 1: full blob 권한을 사용 하 여 blob SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="9485e-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="9485e-113">이 예제에서는 full blob 권한이 있는 blob SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="9485e-114">예제 2: 수명 기간 동안 blob SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="9485e-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="9485e-115">이 예제에서는 수명 기간 동안 blob SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="9485e-116">변수</span><span class="sxs-lookup"><span data-stu-id="9485e-116">PARAMETERS</span></span>

### <span data-ttu-id="9485e-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="9485e-117">-Blob</span></span>
<span data-ttu-id="9485e-118">저장소 blob 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-118">Specifies the storage blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9485e-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9485e-119">-CloudBlob</span></span>
<span data-ttu-id="9485e-120">**CloudBlob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="9485e-121">**CloudBlob** 개체를 가져오려면 [Get-azurestorageblob](./Get-AzureStorageBlob.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9485e-122">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="9485e-122">-Container</span></span>
<span data-ttu-id="9485e-123">저장소 컨테이너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-123">Specifies the storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9485e-124">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="9485e-124">-Context</span></span>
<span data-ttu-id="9485e-125">저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-125">Specifies the storage context.</span></span>

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

### <span data-ttu-id="9485e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9485e-126">-DefaultProfile</span></span>
<span data-ttu-id="9485e-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9485e-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9485e-128">-ExpiryTime</span></span>
<span data-ttu-id="9485e-129">공유 액세스 서명이 만료 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-129">Specifies when the shared access signature expires.</span></span>

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

### <span data-ttu-id="9485e-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="9485e-130">-FullUri</span></span>
<span data-ttu-id="9485e-131">이 cmdlet이 full blob URI 및 공유 액세스 서명 토큰을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="9485e-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="9485e-132">-IPAddressOrRange</span></span>
<span data-ttu-id="9485e-133">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="9485e-134">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="9485e-135">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="9485e-135">-Permission</span></span>
<span data-ttu-id="9485e-136">저장소 blob에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-136">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="9485e-137">이는 문자열 (예: `rwd` 읽기, 쓰기 및 삭제) 이라고 한다는 점에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-137">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9485e-138">-정책</span><span class="sxs-lookup"><span data-stu-id="9485e-138">-Policy</span></span>
<span data-ttu-id="9485e-139">Azure 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-139">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9485e-140">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="9485e-140">-Protocol</span></span>
<span data-ttu-id="9485e-141">요청에 허용 된 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-141">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="9485e-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-142">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="9485e-143">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="9485e-143">HttpsOnly</span></span>
* <span data-ttu-id="9485e-144">HttpsOrHttp의 기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-144">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9485e-145">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9485e-145">-StartTime</span></span>
<span data-ttu-id="9485e-146">공유 액세스 서명이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-146">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="9485e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9485e-147">CommonParameters</span></span>
<span data-ttu-id="9485e-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9485e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9485e-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9485e-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9485e-150">입력</span><span class="sxs-lookup"><span data-stu-id="9485e-150">INPUTS</span></span>

### <span data-ttu-id="9485e-151">WindowsAzure. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9485e-151">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="9485e-152">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9485e-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9485e-153">출력</span><span class="sxs-lookup"><span data-stu-id="9485e-153">OUTPUTS</span></span>

### <span data-ttu-id="9485e-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9485e-154">System.String</span></span>

## <span data-ttu-id="9485e-155">상속자</span><span class="sxs-lookup"><span data-stu-id="9485e-155">NOTES</span></span>

## <span data-ttu-id="9485e-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9485e-156">RELATED LINKS</span></span>

[<span data-ttu-id="9485e-157">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9485e-157">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="9485e-158">새로운 AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="9485e-158">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)