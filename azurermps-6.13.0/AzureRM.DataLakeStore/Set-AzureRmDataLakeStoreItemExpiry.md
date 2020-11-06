---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: 4aff82a2621a462f0af14fe2dce620f297011874
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529618"
---
# <span data-ttu-id="66b7f-101">Set-AzureRmDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="66b7f-101">Set-AzureRmDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="66b7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="66b7f-103">Azure Data Lake Store 계정에서 파일의 만료 시간을 설정 하거나 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="66b7f-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66b7f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="66b7f-104">SYNTAX</span></span>

### <span data-ttu-id="66b7f-105">SetAbsoluteNeverExpireExpiry (기본값)</span><span class="sxs-lookup"><span data-stu-id="66b7f-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66b7f-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="66b7f-106">SetRelativeExpiry</span></span>
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66b7f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="66b7f-107">DESCRIPTION</span></span>
<span data-ttu-id="66b7f-108">**AzureRmDataLakeStoreItemExpiry** Cmdlet은 Azure Data Lake store 계정에서 파일의 만료 시간을 설정 하거나 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="66b7f-108">The **Set-AzureRmDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="66b7f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="66b7f-109">EXAMPLES</span></span>

### <span data-ttu-id="66b7f-110">예제 1: 파일의 만료 시간 설정</span><span class="sxs-lookup"><span data-stu-id="66b7f-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="66b7f-111">계정 ContosoADL의 파일 myfile.txt에서 만료를 2 시간으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66b7f-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="66b7f-112">이렇게 하면 두 시간 후에 파일이 만료 됩니다 (삭제 하도록 표시 됨).</span><span class="sxs-lookup"><span data-stu-id="66b7f-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="66b7f-113">예제 2: 파일에서 만료 제거</span><span class="sxs-lookup"><span data-stu-id="66b7f-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="66b7f-114">' ContosoADL ' 계정에서 ' myfile.txt ' 파일에 대해 이전에 설정 된 만료를 모두 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="66b7f-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="66b7f-115">즉, 파일이 자동으로 만료 (삭제로 표시 됨) 되며 수동으로 삭제 하거나 만료 되도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66b7f-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="66b7f-116">예제 3: 현재 위치에 상대적인 파일의 만료 시간 설정</span><span class="sxs-lookup"><span data-stu-id="66b7f-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="66b7f-117">첫 번째 명령은 서버에서 현재 시간을 기준으로 240 초의 파일/myfile.txt 만료 시간을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66b7f-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="66b7f-118">두 번째 명령은 서버에서 만든 시간을 기준으로 240 초 동안 myfile.txt 파일의 만료 시간을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66b7f-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="66b7f-119">변수</span><span class="sxs-lookup"><span data-stu-id="66b7f-119">PARAMETERS</span></span>

### <span data-ttu-id="66b7f-120">-계정</span><span class="sxs-lookup"><span data-stu-id="66b7f-120">-Account</span></span>
<span data-ttu-id="66b7f-121">Data Lake Store 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66b7f-121">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="66b7f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b7f-122">-DefaultProfile</span></span>
<span data-ttu-id="66b7f-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66b7f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66b7f-124">-만료</span><span class="sxs-lookup"><span data-stu-id="66b7f-124">-Expiration</span></span>
<span data-ttu-id="66b7f-125">지정 된 파일의 절대 만료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="66b7f-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="66b7f-126">값이 없거나 MaxValue로 설정 되어 있으면 파일이 만료 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66b7f-126">If no value or set to MaxValue, the file will never expire.</span></span>

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

### <span data-ttu-id="66b7f-127">-Path</span><span class="sxs-lookup"><span data-stu-id="66b7f-127">-Path</span></span>
<span data-ttu-id="66b7f-128">만료를 설정 하거나 제거할 파일 항목의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66b7f-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

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

### <span data-ttu-id="66b7f-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="66b7f-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="66b7f-130">상대 만료 옵션</span><span class="sxs-lookup"><span data-stu-id="66b7f-130">Relative expiry options.</span></span> <span data-ttu-id="66b7f-131">RelativeToNow 또는 RelativeToCreationDate는 현재 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="66b7f-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

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

### <span data-ttu-id="66b7f-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="66b7f-132">-RelativeTime</span></span>
<span data-ttu-id="66b7f-133">현재 또는 생성 시간에 대 한 밀리초 단위의 상대 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="66b7f-133">The relative time in milliseconds with respect to now or creation time</span></span>

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

### <span data-ttu-id="66b7f-134">-확인</span><span class="sxs-lookup"><span data-stu-id="66b7f-134">-Confirm</span></span>
<span data-ttu-id="66b7f-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="66b7f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66b7f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66b7f-136">-WhatIf</span></span>
<span data-ttu-id="66b7f-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="66b7f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66b7f-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66b7f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66b7f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b7f-139">CommonParameters</span></span>
<span data-ttu-id="66b7f-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="66b7f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b7f-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66b7f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b7f-142">입력</span><span class="sxs-lookup"><span data-stu-id="66b7f-142">INPUTS</span></span>

### <span data-ttu-id="66b7f-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="66b7f-143">System.String</span></span>

### <span data-ttu-id="66b7f-144">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="66b7f-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="66b7f-145">시스템 DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="66b7f-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="66b7f-146">DataLakeStore. DataLakeStoreEnums + PathRelativeExpiryOptions.</span><span class="sxs-lookup"><span data-stu-id="66b7f-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="66b7f-147">시스템 Int64</span><span class="sxs-lookup"><span data-stu-id="66b7f-147">System.Int64</span></span>

## <span data-ttu-id="66b7f-148">출력</span><span class="sxs-lookup"><span data-stu-id="66b7f-148">OUTPUTS</span></span>

### <span data-ttu-id="66b7f-149">DataLakeStore. DataLakeStoreItem/.</span><span class="sxs-lookup"><span data-stu-id="66b7f-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="66b7f-150">상속자</span><span class="sxs-lookup"><span data-stu-id="66b7f-150">NOTES</span></span>
<span data-ttu-id="66b7f-151">별칭: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="66b7f-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="66b7f-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66b7f-152">RELATED LINKS</span></span>

[<span data-ttu-id="66b7f-153">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="66b7f-153">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

