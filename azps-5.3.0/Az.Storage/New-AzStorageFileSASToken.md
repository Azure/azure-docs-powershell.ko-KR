---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
ms.openlocfilehash: fcd58edbb3d6e03becc8e6305f58555fedf36107
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491335"
---
# <span data-ttu-id="94ab3-101">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="94ab3-101">New-AzStorageFileSASToken</span></span>

## <span data-ttu-id="94ab3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="94ab3-103">Storage 파일에 대한 공유 액세스 서명 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="94ab3-104">구문</span><span class="sxs-lookup"><span data-stu-id="94ab3-104">SYNTAX</span></span>

### <span data-ttu-id="94ab3-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="94ab3-105">NameSasPermission</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="94ab3-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="94ab3-106">NameSasPolicy</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="94ab3-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="94ab3-107">FileSasPermission</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94ab3-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="94ab3-108">FileSasPolicy</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94ab3-109">설명</span><span class="sxs-lookup"><span data-stu-id="94ab3-109">DESCRIPTION</span></span>
<span data-ttu-id="94ab3-110">**New-AzStorageFileSASToken** cmdlet은 Azure Storage 파일에 대한 공유 액세스 서명 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-110">The **New-AzStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="94ab3-111">예제</span><span class="sxs-lookup"><span data-stu-id="94ab3-111">EXAMPLES</span></span>

### <span data-ttu-id="94ab3-112">예제 1: 전체 파일 권한이 있는 공유 액세스 서명 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="94ab3-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="94ab3-113">이 명령은 FilePath라는 파일에 대한 모든 권한이 있는 공유 액세스 서명 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="94ab3-114">예제 2: 시간 제한이 있는 공유 액세스 서명 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="94ab3-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="94ab3-115">첫 번째 명령은 Get-Date cmdlet을 사용하여 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="94ab3-116">이 명령은 현재 시간을 $StartTime 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="94ab3-117">두 번째 명령은 $StartTime 개체에 2시간을 추가한 다음, 결과를 $EndTime 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="94ab3-118">이 개체는 향후 2시간의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="94ab3-119">세 번째 명령은 지정된 권한이 있는 공유 액세스 서명 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="94ab3-120">이 토큰은 현재 시간에서 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="94ab3-121">토큰은 토큰에 저장된 시간이 될 때까지 $EndTime.</span><span class="sxs-lookup"><span data-stu-id="94ab3-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="94ab3-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94ab3-122">PARAMETERS</span></span>

### <span data-ttu-id="94ab3-123">-Context</span><span class="sxs-lookup"><span data-stu-id="94ab3-123">-Context</span></span>
<span data-ttu-id="94ab3-124">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="94ab3-125">컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-125">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="94ab3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ab3-126">-DefaultProfile</span></span>
<span data-ttu-id="94ab3-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94ab3-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="94ab3-128">-ExpiryTime</span></span>
<span data-ttu-id="94ab3-129">공유 액세스 서명이 유효하지 않은 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="94ab3-130">-File</span><span class="sxs-lookup"><span data-stu-id="94ab3-130">-File</span></span>
<span data-ttu-id="94ab3-131">**CloudFile** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="94ab3-132">클라우드 파일을 만들거나 다음 cmdlet을 사용하여 Get-AzStorageFile 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases: CloudFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94ab3-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="94ab3-133">-FullUri</span></span>
<span data-ttu-id="94ab3-134">이 cmdlet이 전체 Blob URI 및 공유 액세스 서명 토큰을 반환하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="94ab3-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="94ab3-135">-IPAddressOrRange</span></span>
<span data-ttu-id="94ab3-136">요청을 수락할 IP 주소 또는 IP 주소 범위를 지정합니다(예: 168.1.5.65 또는 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="94ab3-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="94ab3-137">범위는 포괄적입니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="94ab3-138">-Path</span><span class="sxs-lookup"><span data-stu-id="94ab3-138">-Path</span></span>
<span data-ttu-id="94ab3-139">Storage 공유를 상대로 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-139">Specifies the path of the file relative to a Storage share.</span></span>

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

### <span data-ttu-id="94ab3-140">-Permission</span><span class="sxs-lookup"><span data-stu-id="94ab3-140">-Permission</span></span>
<span data-ttu-id="94ab3-141">Storage 파일에 대한 권한을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="94ab3-142">이 문자열은 읽기, 쓰기 및 삭제와 같은 `rwd` 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="94ab3-143">-Policy</span><span class="sxs-lookup"><span data-stu-id="94ab3-143">-Policy</span></span>
<span data-ttu-id="94ab3-144">파일에 대해 저장된 액세스 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-144">Specifies the stored access policy for a file.</span></span>

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

### <span data-ttu-id="94ab3-145">-Protocol</span><span class="sxs-lookup"><span data-stu-id="94ab3-145">-Protocol</span></span>
<span data-ttu-id="94ab3-146">요청에 허용되는 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="94ab3-147">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="94ab3-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="94ab3-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="94ab3-148">HttpsOnly</span></span>
* <span data-ttu-id="94ab3-149">HttpsOrHttp 기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="94ab3-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="94ab3-150">-ShareName</span></span>
<span data-ttu-id="94ab3-151">저장소 공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-151">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="94ab3-152">-StartTime</span><span class="sxs-lookup"><span data-stu-id="94ab3-152">-StartTime</span></span>
<span data-ttu-id="94ab3-153">공유 액세스 서명이 유효한 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-153">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="94ab3-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ab3-154">CommonParameters</span></span>
<span data-ttu-id="94ab3-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="94ab3-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ab3-156">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="94ab3-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ab3-157">입력</span><span class="sxs-lookup"><span data-stu-id="94ab3-157">INPUTS</span></span>

### <span data-ttu-id="94ab3-158">System.String</span><span class="sxs-lookup"><span data-stu-id="94ab3-158">System.String</span></span>

### <span data-ttu-id="94ab3-159">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="94ab3-159">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="94ab3-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="94ab3-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="94ab3-161">출력</span><span class="sxs-lookup"><span data-stu-id="94ab3-161">OUTPUTS</span></span>

### <span data-ttu-id="94ab3-162">System.String</span><span class="sxs-lookup"><span data-stu-id="94ab3-162">System.String</span></span>

## <span data-ttu-id="94ab3-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="94ab3-163">NOTES</span></span>

## <span data-ttu-id="94ab3-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94ab3-164">RELATED LINKS</span></span>

[<span data-ttu-id="94ab3-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="94ab3-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="94ab3-166">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="94ab3-166">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)
