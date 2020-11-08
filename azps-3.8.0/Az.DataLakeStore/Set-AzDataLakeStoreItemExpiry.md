---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: ff769801c7a3496ab094e5c9877e0b53fb64fbfd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94045027"
---
# <span data-ttu-id="f042d-101">Set-AzDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="f042d-101">Set-AzDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="f042d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f042d-102">SYNOPSIS</span></span>
<span data-ttu-id="f042d-103">Azure Data Lake Store 계정에서 파일의 만료 시간을 설정 하거나 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f042d-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="f042d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f042d-104">SYNTAX</span></span>

### <span data-ttu-id="f042d-105">SetAbsoluteNeverExpireExpiry (기본값)</span><span class="sxs-lookup"><span data-stu-id="f042d-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f042d-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="f042d-106">SetRelativeExpiry</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f042d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f042d-107">DESCRIPTION</span></span>
<span data-ttu-id="f042d-108">**AzDataLakeStoreItemExpiry** Cmdlet은 Azure Data Lake store 계정에서 파일의 만료 시간을 설정 하거나 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f042d-108">The **Set-AzDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="f042d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f042d-109">EXAMPLES</span></span>

### <span data-ttu-id="f042d-110">예제 1: 파일의 만료 시간 설정</span><span class="sxs-lookup"><span data-stu-id="f042d-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="f042d-111">계정 ContosoADL의 파일 myfile.txt에서 만료를 2 시간으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f042d-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="f042d-112">이렇게 하면 두 시간 후에 파일이 만료 됩니다 (삭제 하도록 표시 됨).</span><span class="sxs-lookup"><span data-stu-id="f042d-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="f042d-113">예제 2: 파일에서 만료 제거</span><span class="sxs-lookup"><span data-stu-id="f042d-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="f042d-114">' ContosoADL ' 계정에서 ' myfile.txt ' 파일에 대해 이전에 설정 된 만료를 모두 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f042d-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="f042d-115">즉, 파일이 자동으로 만료 (삭제로 표시 됨) 되며 수동으로 삭제 하거나 만료 되도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f042d-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="f042d-116">예제 3: 현재 위치에 상대적인 파일의 만료 시간 설정</span><span class="sxs-lookup"><span data-stu-id="f042d-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="f042d-117">첫 번째 명령은 서버에서 현재 시간을 기준으로 240 초의 파일/myfile.txt 만료 시간을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f042d-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="f042d-118">두 번째 명령은 서버에서 만든 시간을 기준으로 240 초 동안 myfile.txt 파일의 만료 시간을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f042d-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="f042d-119">변수</span><span class="sxs-lookup"><span data-stu-id="f042d-119">PARAMETERS</span></span>

### <span data-ttu-id="f042d-120">-계정</span><span class="sxs-lookup"><span data-stu-id="f042d-120">-Account</span></span>
<span data-ttu-id="f042d-121">Data Lake Store 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f042d-121">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="f042d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f042d-122">-DefaultProfile</span></span>
<span data-ttu-id="f042d-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f042d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f042d-124">-만료</span><span class="sxs-lookup"><span data-stu-id="f042d-124">-Expiration</span></span>
<span data-ttu-id="f042d-125">지정 된 파일의 절대 만료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="f042d-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="f042d-126">값이 없거나 MaxValue로 설정 되어 있으면 파일이 만료 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f042d-126">If no value or set to MaxValue, the file will never expire.</span></span>

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

### <span data-ttu-id="f042d-127">-Path</span><span class="sxs-lookup"><span data-stu-id="f042d-127">-Path</span></span>
<span data-ttu-id="f042d-128">만료를 설정 하거나 제거할 파일 항목의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f042d-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

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

### <span data-ttu-id="f042d-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="f042d-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="f042d-130">상대 만료 옵션</span><span class="sxs-lookup"><span data-stu-id="f042d-130">Relative expiry options.</span></span> <span data-ttu-id="f042d-131">RelativeToNow 또는 RelativeToCreationDate는 현재 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="f042d-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

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

### <span data-ttu-id="f042d-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="f042d-132">-RelativeTime</span></span>
<span data-ttu-id="f042d-133">현재 또는 생성 시간에 대 한 밀리초 단위의 상대 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="f042d-133">The relative time in milliseconds with respect to now or creation time</span></span>

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

### <span data-ttu-id="f042d-134">-확인</span><span class="sxs-lookup"><span data-stu-id="f042d-134">-Confirm</span></span>
<span data-ttu-id="f042d-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f042d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f042d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f042d-136">-WhatIf</span></span>
<span data-ttu-id="f042d-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f042d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f042d-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f042d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f042d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f042d-139">CommonParameters</span></span>
<span data-ttu-id="f042d-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f042d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f042d-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f042d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f042d-142">입력</span><span class="sxs-lookup"><span data-stu-id="f042d-142">INPUTS</span></span>

### <span data-ttu-id="f042d-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f042d-143">System.String</span></span>

### <span data-ttu-id="f042d-144">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="f042d-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="f042d-145">시스템 DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f042d-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="f042d-146">DataLakeStore. DataLakeStoreEnums + PathRelativeExpiryOptions.</span><span class="sxs-lookup"><span data-stu-id="f042d-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="f042d-147">시스템 Int64</span><span class="sxs-lookup"><span data-stu-id="f042d-147">System.Int64</span></span>

## <span data-ttu-id="f042d-148">출력</span><span class="sxs-lookup"><span data-stu-id="f042d-148">OUTPUTS</span></span>

### <span data-ttu-id="f042d-149">DataLakeStore. DataLakeStoreItem/.</span><span class="sxs-lookup"><span data-stu-id="f042d-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="f042d-150">상속자</span><span class="sxs-lookup"><span data-stu-id="f042d-150">NOTES</span></span>
<span data-ttu-id="f042d-151">별칭: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="f042d-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="f042d-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f042d-152">RELATED LINKS</span></span>

[<span data-ttu-id="f042d-153">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f042d-153">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

