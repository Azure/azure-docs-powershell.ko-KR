---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
ms.openlocfilehash: b38f7d0463062f07e425decae98f8b6acba8c4ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044687"
---
# <span data-ttu-id="14c53-101">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="14c53-101">New-AzStorageFileSASToken</span></span>

## <span data-ttu-id="14c53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14c53-102">SYNOPSIS</span></span>
<span data-ttu-id="14c53-103">저장소 파일에 대 한 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="14c53-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14c53-104">SYNTAX</span></span>

### <span data-ttu-id="14c53-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="14c53-105">NameSasPermission</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14c53-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="14c53-106">NameSasPolicy</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14c53-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="14c53-107">FileSasPermission</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14c53-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="14c53-108">FileSasPolicy</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14c53-109">설명은</span><span class="sxs-lookup"><span data-stu-id="14c53-109">DESCRIPTION</span></span>
<span data-ttu-id="14c53-110">**AzStorageFileSASToken** Cmdlet은 Azure 저장소 파일에 대 한 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-110">The **New-AzStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="14c53-111">예제의</span><span class="sxs-lookup"><span data-stu-id="14c53-111">EXAMPLES</span></span>

### <span data-ttu-id="14c53-112">예제 1: 전체 파일 사용 권한이 있는 공유 액세스 서명 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="14c53-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="14c53-113">이 명령은 이름이 FilePath 인 파일에 대 한 모든 권한이 있는 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="14c53-114">예제 2: 시간 제한이 있는 공유 액세스 서명 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="14c53-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="14c53-115">첫 번째 명령은 Get-Date cmdlet을 사용 하 여 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="14c53-116">명령이 현재 시간을 $StartTime 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="14c53-117">두 번째 명령은 $StartTime에서 개체에 두 시간을 추가한 다음 결과를 $EndTime 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="14c53-118">이 개체는 향후 2 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="14c53-119">세 번째 명령은 지정 된 사용 권한이 있는 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="14c53-120">이 토큰은 현재 시간에 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="14c53-121">토큰은 $EndTime에 저장 된 시간까지 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="14c53-122">변수</span><span class="sxs-lookup"><span data-stu-id="14c53-122">PARAMETERS</span></span>

### <span data-ttu-id="14c53-123">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="14c53-123">-Context</span></span>
<span data-ttu-id="14c53-124">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="14c53-125">컨텍스트를 가져오려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-125">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14c53-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c53-126">-DefaultProfile</span></span>
<span data-ttu-id="14c53-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14c53-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="14c53-128">-ExpiryTime</span></span>
<span data-ttu-id="14c53-129">공유 액세스 서명이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="14c53-130">-파일</span><span class="sxs-lookup"><span data-stu-id="14c53-130">-File</span></span>
<span data-ttu-id="14c53-131">**Cloudfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="14c53-132">클라우드 파일을 만들거나 Get-AzStorageFile cmdlet을 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14c53-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="14c53-133">-FullUri</span></span>
<span data-ttu-id="14c53-134">이 cmdlet이 full blob URI 및 공유 액세스 서명 토큰을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="14c53-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="14c53-135">-IPAddressOrRange</span></span>
<span data-ttu-id="14c53-136">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="14c53-137">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="14c53-138">-Path</span><span class="sxs-lookup"><span data-stu-id="14c53-138">-Path</span></span>
<span data-ttu-id="14c53-139">저장소 공유에 상대적인 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-139">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14c53-140">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="14c53-140">-Permission</span></span>
<span data-ttu-id="14c53-141">저장소 파일에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="14c53-142">이는 문자열 (예: `rwd` 읽기, 쓰기 및 삭제) 이라고 한다는 점에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14c53-143">-정책</span><span class="sxs-lookup"><span data-stu-id="14c53-143">-Policy</span></span>
<span data-ttu-id="14c53-144">파일에 대 한 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-144">Specifies the stored access policy for a file.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14c53-145">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="14c53-145">-Protocol</span></span>
<span data-ttu-id="14c53-146">요청에 허용 된 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="14c53-147">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="14c53-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="14c53-148">HttpsOnly</span></span>
* <span data-ttu-id="14c53-149">HttpsOrHttp의 기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="14c53-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="14c53-150">-ShareName</span></span>
<span data-ttu-id="14c53-151">저장소 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-151">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14c53-152">-StartTime</span><span class="sxs-lookup"><span data-stu-id="14c53-152">-StartTime</span></span>
<span data-ttu-id="14c53-153">공유 액세스 서명이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-153">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="14c53-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c53-154">CommonParameters</span></span>
<span data-ttu-id="14c53-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c53-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c53-156">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14c53-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c53-157">입력</span><span class="sxs-lookup"><span data-stu-id="14c53-157">INPUTS</span></span>

### <span data-ttu-id="14c53-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="14c53-158">System.String</span></span>

### <span data-ttu-id="14c53-159">Microsoft. c c. | 파일</span><span class="sxs-lookup"><span data-stu-id="14c53-159">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="14c53-160">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="14c53-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="14c53-161">출력</span><span class="sxs-lookup"><span data-stu-id="14c53-161">OUTPUTS</span></span>

### <span data-ttu-id="14c53-162">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="14c53-162">System.String</span></span>

## <span data-ttu-id="14c53-163">상속자</span><span class="sxs-lookup"><span data-stu-id="14c53-163">NOTES</span></span>

## <span data-ttu-id="14c53-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14c53-164">RELATED LINKS</span></span>

[<span data-ttu-id="14c53-165">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="14c53-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="14c53-166">새로운 AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="14c53-166">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)
