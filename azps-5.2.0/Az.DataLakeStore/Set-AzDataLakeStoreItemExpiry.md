---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: ff769801c7a3496ab094e5c9877e0b53fb64fbfd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356241"
---
# <span data-ttu-id="0a40d-101">Set-AzDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="0a40d-101">Set-AzDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="0a40d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a40d-102">SYNOPSIS</span></span>
<span data-ttu-id="0a40d-103">Azure Data Lake Store 계정의 파일에 대한 만료 시간을 설정하거나 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0a40d-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="0a40d-104">구문</span><span class="sxs-lookup"><span data-stu-id="0a40d-104">SYNTAX</span></span>

### <span data-ttu-id="0a40d-105">SetAbsoluteNeverExpireExpiry(기본값)</span><span class="sxs-lookup"><span data-stu-id="0a40d-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a40d-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="0a40d-106">SetRelativeExpiry</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a40d-107">설명</span><span class="sxs-lookup"><span data-stu-id="0a40d-107">DESCRIPTION</span></span>
<span data-ttu-id="0a40d-108">**Set-AzDataLakeStoreItemExpiry** cmdlet은 Azure Data Lake Store 계정의 파일에 대한 만료 시간을 설정하거나 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0a40d-108">The **Set-AzDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="0a40d-109">예제</span><span class="sxs-lookup"><span data-stu-id="0a40d-109">EXAMPLES</span></span>

### <span data-ttu-id="0a40d-110">예제 1: 파일의 만료 시간 설정</span><span class="sxs-lookup"><span data-stu-id="0a40d-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="0a40d-111">ContosoADL 계정의 myfile.txt 만료를 지금부터 2시간으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0a40d-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="0a40d-112">이렇게 하면 파일이 2시간 후에 만료됩니다(삭제로 표시).</span><span class="sxs-lookup"><span data-stu-id="0a40d-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="0a40d-113">예제 2: 파일의 만료 제거</span><span class="sxs-lookup"><span data-stu-id="0a40d-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="0a40d-114">이전에 'ContosoADL' 계정의 'myfile.txt'에 설정된 만료를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0a40d-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="0a40d-115">즉, 파일이 자동으로 만료되지 않습니다(삭제로 표시). 수동으로 삭제하거나 다시 만료로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a40d-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="0a40d-116">예제 3: 현재와 상대적인 파일의 만료 시간 설정</span><span class="sxs-lookup"><span data-stu-id="0a40d-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="0a40d-117">첫 번째 명령은 서버의 현재 시간을 myfile.txt /myfile.txt 파일의 만료 시간을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0a40d-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="0a40d-118">두 번째 명령은 서버에서 생성 시간을 myfile.txt /myfile.txt 파일의 만료 시간을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0a40d-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="0a40d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a40d-119">PARAMETERS</span></span>

### <span data-ttu-id="0a40d-120">-Account</span><span class="sxs-lookup"><span data-stu-id="0a40d-120">-Account</span></span>
<span data-ttu-id="0a40d-121">Data Lake Store 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0a40d-121">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a40d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a40d-122">-DefaultProfile</span></span>
<span data-ttu-id="0a40d-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a40d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a40d-124">-Expiration</span><span class="sxs-lookup"><span data-stu-id="0a40d-124">-Expiration</span></span>
<span data-ttu-id="0a40d-125">지정된 파일의 절대 만료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="0a40d-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="0a40d-126">값이 아니거나 MaxValue로 설정된 경우 파일이 만료되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a40d-126">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: SetAbsoluteNeverExpireExpiry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a40d-127">-Path</span><span class="sxs-lookup"><span data-stu-id="0a40d-127">-Path</span></span>
<span data-ttu-id="0a40d-128">만료를 설정하거나 제거할 파일 항목의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0a40d-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a40d-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="0a40d-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="0a40d-130">상대적 만료 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="0a40d-130">Relative expiry options.</span></span> <span data-ttu-id="0a40d-131">RelativeToNow 또는 RelativeToCreationDate는 현재 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="0a40d-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions
Parameter Sets: SetRelativeExpiry
Aliases:
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a40d-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="0a40d-132">-RelativeTime</span></span>
<span data-ttu-id="0a40d-133">현재 또는 생성 시간과 관련한 상대 시간(밀리초)</span><span class="sxs-lookup"><span data-stu-id="0a40d-133">The relative time in milliseconds with respect to now or creation time</span></span>

```yaml
Type: System.Int64
Parameter Sets: SetRelativeExpiry
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a40d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a40d-134">-Confirm</span></span>
<span data-ttu-id="0a40d-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a40d-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a40d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a40d-136">-WhatIf</span></span>
<span data-ttu-id="0a40d-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0a40d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a40d-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a40d-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a40d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a40d-139">CommonParameters</span></span>
<span data-ttu-id="0a40d-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0a40d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a40d-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0a40d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a40d-142">입력</span><span class="sxs-lookup"><span data-stu-id="0a40d-142">INPUTS</span></span>

### <span data-ttu-id="0a40d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="0a40d-143">System.String</span></span>

### <span data-ttu-id="0a40d-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="0a40d-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="0a40d-145">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0a40d-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="0a40d-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span><span class="sxs-lookup"><span data-stu-id="0a40d-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="0a40d-147">System.Int64</span><span class="sxs-lookup"><span data-stu-id="0a40d-147">System.Int64</span></span>

## <span data-ttu-id="0a40d-148">출력</span><span class="sxs-lookup"><span data-stu-id="0a40d-148">OUTPUTS</span></span>

### <span data-ttu-id="0a40d-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0a40d-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="0a40d-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0a40d-150">NOTES</span></span>
<span data-ttu-id="0a40d-151">별칭: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="0a40d-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="0a40d-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a40d-152">RELATED LINKS</span></span>

[<span data-ttu-id="0a40d-153">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0a40d-153">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

