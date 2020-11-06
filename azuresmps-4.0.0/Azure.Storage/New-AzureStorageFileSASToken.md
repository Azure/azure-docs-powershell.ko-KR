---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19d3017ffdff2ebc0f0c8d614b5b9c4d4b0514d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523672"
---
# <span data-ttu-id="2570b-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="2570b-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="2570b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2570b-102">SYNOPSIS</span></span>
<span data-ttu-id="2570b-103">저장소 파일에 대 한 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="2570b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2570b-104">SYNTAX</span></span>

### <span data-ttu-id="2570b-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="2570b-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="2570b-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="2570b-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="2570b-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="2570b-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

### <span data-ttu-id="2570b-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="2570b-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

## <span data-ttu-id="2570b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="2570b-109">DESCRIPTION</span></span>
<span data-ttu-id="2570b-110">**AzureStorageFileSASToken** Cmdlet은 Azure 저장소 파일에 대 한 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="2570b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2570b-111">EXAMPLES</span></span>

### <span data-ttu-id="2570b-112">예제 1: 전체 파일 사용 권한이 있는 공유 액세스 서명 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="2570b-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="2570b-113">이 명령은 이름이 FilePath 인 파일에 대 한 모든 권한이 있는 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="2570b-114">예제 2: 시간 제한이 있는 공유 액세스 서명 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="2570b-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="2570b-115">첫 번째 명령은 Get-Date cmdlet을 사용 하 여 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="2570b-116">명령이 현재 시간을 $StartTime 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-116">The command stores the current time in the $StartTime variable.</span></span>

<span data-ttu-id="2570b-117">두 번째 명령은 $StartTime에서 개체에 두 시간을 추가한 다음 결과를 $EndTime 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="2570b-118">이 개체는 향후 2 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-118">This object is a time two hours in the future.</span></span>

<span data-ttu-id="2570b-119">세 번째 명령은 지정 된 사용 권한이 있는 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="2570b-120">이 토큰은 현재 시간에 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="2570b-121">토큰은 $EndTime에 저장 된 시간까지 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="2570b-122">변수</span><span class="sxs-lookup"><span data-stu-id="2570b-122">PARAMETERS</span></span>

### <span data-ttu-id="2570b-123">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="2570b-123">-Context</span></span>
<span data-ttu-id="2570b-124">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="2570b-125">컨텍스트를 가져오려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2570b-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2570b-126">-ExpiryTime</span></span>
<span data-ttu-id="2570b-127">공유 액세스 서명이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-127">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="2570b-128">-파일</span><span class="sxs-lookup"><span data-stu-id="2570b-128">-File</span></span>
<span data-ttu-id="2570b-129">**Cloudfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="2570b-130">클라우드 파일을 만들거나 Get-AzureStorageFile cmdlet을 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="2570b-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="2570b-131">-FullUri</span></span>
<span data-ttu-id="2570b-132">이 cmdlet이 full blob URI 및 공유 액세스 서명 토큰을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-132">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="2570b-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="2570b-133">-IPAddressOrRange</span></span>
<span data-ttu-id="2570b-134">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="2570b-135">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="2570b-136">-Path</span><span class="sxs-lookup"><span data-stu-id="2570b-136">-Path</span></span>
<span data-ttu-id="2570b-137">저장소 공유에 상대적인 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-137">Specifies the path of the file relative to a Storage share.</span></span>

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

### <span data-ttu-id="2570b-138">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="2570b-138">-Permission</span></span>
<span data-ttu-id="2570b-139">저장소 파일에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-139">Specifies the permissions for a Storage file.</span></span>

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

### <span data-ttu-id="2570b-140">-정책</span><span class="sxs-lookup"><span data-stu-id="2570b-140">-Policy</span></span>
<span data-ttu-id="2570b-141">파일에 대 한 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-141">Specifies the stored access policy for a file.</span></span>

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

### <span data-ttu-id="2570b-142">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="2570b-142">-Protocol</span></span>
<span data-ttu-id="2570b-143">요청에 허용 된 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="2570b-144">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="2570b-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="2570b-145">HttpsOnly</span></span>
* <span data-ttu-id="2570b-146">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="2570b-146">HttpsOrHttp</span></span>

<span data-ttu-id="2570b-147">기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-147">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="2570b-148">-ShareName</span><span class="sxs-lookup"><span data-stu-id="2570b-148">-ShareName</span></span>
<span data-ttu-id="2570b-149">저장소 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-149">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="2570b-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2570b-150">-StartTime</span></span>
<span data-ttu-id="2570b-151">공유 액세스 서명이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-151">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="2570b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2570b-152">CommonParameters</span></span>
<span data-ttu-id="2570b-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2570b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2570b-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2570b-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2570b-155">입력</span><span class="sxs-lookup"><span data-stu-id="2570b-155">INPUTS</span></span>

## <span data-ttu-id="2570b-156">출력</span><span class="sxs-lookup"><span data-stu-id="2570b-156">OUTPUTS</span></span>

## <span data-ttu-id="2570b-157">상속자</span><span class="sxs-lookup"><span data-stu-id="2570b-157">NOTES</span></span>

## <span data-ttu-id="2570b-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2570b-158">RELATED LINKS</span></span>

[<span data-ttu-id="2570b-159">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="2570b-159">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="2570b-160">새로운 AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="2570b-160">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
