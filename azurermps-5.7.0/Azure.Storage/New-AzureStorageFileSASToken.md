---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
ms.openlocfilehash: e5e4eaf5fa6808432dfdb04120bf9ef92a98452b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530608"
---
# <span data-ttu-id="b84eb-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="b84eb-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="b84eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b84eb-102">SYNOPSIS</span></span>
<span data-ttu-id="b84eb-103">저장소 파일에 대 한 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-103">Generates a shared access signature token for a Storage file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b84eb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b84eb-104">SYNTAX</span></span>

### <span data-ttu-id="b84eb-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="b84eb-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="b84eb-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="b84eb-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="b84eb-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="b84eb-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

### <span data-ttu-id="b84eb-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="b84eb-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

## <span data-ttu-id="b84eb-109">설명은</span><span class="sxs-lookup"><span data-stu-id="b84eb-109">DESCRIPTION</span></span>
<span data-ttu-id="b84eb-110">**AzureStorageFileSASToken** Cmdlet은 Azure 저장소 파일에 대 한 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="b84eb-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b84eb-111">EXAMPLES</span></span>

### <span data-ttu-id="b84eb-112">예제 1: 전체 파일 사용 권한이 있는 공유 액세스 서명 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="b84eb-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="b84eb-113">이 명령은 이름이 FilePath 인 파일에 대 한 모든 권한이 있는 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="b84eb-114">예제 2: 시간 제한이 있는 공유 액세스 서명 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="b84eb-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="b84eb-115">첫 번째 명령은 Get-Date cmdlet을 사용 하 여 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="b84eb-116">명령이 현재 시간을 $StartTime 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-116">The command stores the current time in the $StartTime variable.</span></span>

<span data-ttu-id="b84eb-117">두 번째 명령은 $StartTime에서 개체에 두 시간을 추가한 다음 결과를 $EndTime 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="b84eb-118">이 개체는 향후 2 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-118">This object is a time two hours in the future.</span></span>

<span data-ttu-id="b84eb-119">세 번째 명령은 지정 된 사용 권한이 있는 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="b84eb-120">이 토큰은 현재 시간에 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="b84eb-121">토큰은 $EndTime에 저장 된 시간까지 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="b84eb-122">변수</span><span class="sxs-lookup"><span data-stu-id="b84eb-122">PARAMETERS</span></span>

### <span data-ttu-id="b84eb-123">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="b84eb-123">-Context</span></span>
<span data-ttu-id="b84eb-124">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="b84eb-125">컨텍스트를 가져오려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b84eb-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b84eb-126">-ExpiryTime</span></span>
<span data-ttu-id="b84eb-127">공유 액세스 서명이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-127">Specifies the time at which the shared access signature becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84eb-128">-파일</span><span class="sxs-lookup"><span data-stu-id="b84eb-128">-File</span></span>
<span data-ttu-id="b84eb-129">**Cloudfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="b84eb-130">클라우드 파일을 만들거나 Get-AzureStorageFile cmdlet을 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b84eb-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="b84eb-131">-FullUri</span></span>
<span data-ttu-id="b84eb-132">이 cmdlet이 full blob URI 및 공유 액세스 서명 토큰을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-132">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84eb-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="b84eb-133">-IPAddressOrRange</span></span>
<span data-ttu-id="b84eb-134">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="b84eb-135">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-135">The range is inclusive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84eb-136">-Path</span><span class="sxs-lookup"><span data-stu-id="b84eb-136">-Path</span></span>
<span data-ttu-id="b84eb-137">저장소 공유에 상대적인 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-137">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b84eb-138">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="b84eb-138">-Permission</span></span>
<span data-ttu-id="b84eb-139">저장소 파일에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-139">Specifies the permissions for a Storage file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84eb-140">-정책</span><span class="sxs-lookup"><span data-stu-id="b84eb-140">-Policy</span></span>
<span data-ttu-id="b84eb-141">파일에 대 한 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-141">Specifies the stored access policy for a file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84eb-142">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="b84eb-142">-Protocol</span></span>
<span data-ttu-id="b84eb-143">요청에 허용 된 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="b84eb-144">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="b84eb-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="b84eb-145">HttpsOnly</span></span>
* <span data-ttu-id="b84eb-146">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="b84eb-146">HttpsOrHttp</span></span>

<span data-ttu-id="b84eb-147">기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-147">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84eb-148">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b84eb-148">-ShareName</span></span>
<span data-ttu-id="b84eb-149">저장소 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-149">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b84eb-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b84eb-150">-StartTime</span></span>
<span data-ttu-id="b84eb-151">공유 액세스 서명이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-151">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84eb-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b84eb-152">CommonParameters</span></span>
<span data-ttu-id="b84eb-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b84eb-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b84eb-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b84eb-155">입력</span><span class="sxs-lookup"><span data-stu-id="b84eb-155">INPUTS</span></span>

### <span data-ttu-id="b84eb-156">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b84eb-156">IStorageContext</span></span>

<span data-ttu-id="b84eb-157">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-157">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="b84eb-158">CloudFile</span><span class="sxs-lookup"><span data-stu-id="b84eb-158">CloudFile</span></span>

<span data-ttu-id="b84eb-159">' File ' 매개 변수는 파이프라인에서 ' CloudFile ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-159">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="b84eb-160">이름</span><span class="sxs-lookup"><span data-stu-id="b84eb-160">String</span></span>

<span data-ttu-id="b84eb-161">' Path ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-161">Parameter 'Path' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="b84eb-162">이름</span><span class="sxs-lookup"><span data-stu-id="b84eb-162">String</span></span>

<span data-ttu-id="b84eb-163">' ShareName ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b84eb-163">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="b84eb-164">출력</span><span class="sxs-lookup"><span data-stu-id="b84eb-164">OUTPUTS</span></span>

### <span data-ttu-id="b84eb-165">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b84eb-165">System.String</span></span>

## <span data-ttu-id="b84eb-166">상속자</span><span class="sxs-lookup"><span data-stu-id="b84eb-166">NOTES</span></span>

## <span data-ttu-id="b84eb-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b84eb-167">RELATED LINKS</span></span>

[<span data-ttu-id="b84eb-168">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b84eb-168">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="b84eb-169">새로운 AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="b84eb-169">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
