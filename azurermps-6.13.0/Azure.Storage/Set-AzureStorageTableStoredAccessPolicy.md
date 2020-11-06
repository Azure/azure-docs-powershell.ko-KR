---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 80fe36072840d112c4c8849e72deedd0a7f49d25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531531"
---
# <span data-ttu-id="f6540-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f6540-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="f6540-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6540-102">SYNOPSIS</span></span>
<span data-ttu-id="f6540-103">Azure storage 테이블에 대해 저장 된 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6540-103">Sets the stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6540-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f6540-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6540-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f6540-105">DESCRIPTION</span></span>
<span data-ttu-id="f6540-106">**AzureStorageTableStoredAccessPolicy** Cmdlet은 Azure storage 테이블에 대해 저장 된 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6540-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="f6540-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f6540-107">EXAMPLES</span></span>

### <span data-ttu-id="f6540-108">예제 1: 모든 권한이 있는 테이블에서 저장 된 액세스 정책 설정</span><span class="sxs-lookup"><span data-stu-id="f6540-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="f6540-109">이 명령은 MyTable 이라는 저장소 테이블에 대 한 Policy08 라는 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6540-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="f6540-110">변수</span><span class="sxs-lookup"><span data-stu-id="f6540-110">PARAMETERS</span></span>

### <span data-ttu-id="f6540-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="f6540-111">-Context</span></span>
<span data-ttu-id="f6540-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6540-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f6540-113">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6540-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f6540-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6540-114">-DefaultProfile</span></span>
<span data-ttu-id="f6540-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6540-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6540-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f6540-116">-ExpiryTime</span></span>
<span data-ttu-id="f6540-117">저장 된 액세스 정책이 만료 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6540-117">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="f6540-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f6540-118">-NoExpiryTime</span></span>
<span data-ttu-id="f6540-119">액세스 정책에 만료 날짜가 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f6540-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="f6540-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="f6540-120">-NoStartTime</span></span>
<span data-ttu-id="f6540-121">시작 시간이 $Null 설정 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f6540-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="f6540-122">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="f6540-122">-Permission</span></span>
<span data-ttu-id="f6540-123">저장 된 액세스 정책에서 저장소 테이블에 액세스 하는 데 필요한 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6540-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="f6540-124">이는 문자열 (예: `rwd` 읽기, 쓰기 및 삭제) 이라고 한다는 점에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6540-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="f6540-125">-정책</span><span class="sxs-lookup"><span data-stu-id="f6540-125">-Policy</span></span>
<span data-ttu-id="f6540-126">저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6540-126">Specifies the name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6540-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f6540-127">-StartTime</span></span>
<span data-ttu-id="f6540-128">저장 된 액세스 정책이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6540-128">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="f6540-129">-테이블</span><span class="sxs-lookup"><span data-stu-id="f6540-129">-Table</span></span>
<span data-ttu-id="f6540-130">Azure 저장소 테이블 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6540-130">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="f6540-131">-확인</span><span class="sxs-lookup"><span data-stu-id="f6540-131">-Confirm</span></span>
<span data-ttu-id="f6540-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6540-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6540-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6540-133">-WhatIf</span></span>
<span data-ttu-id="f6540-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f6540-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6540-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f6540-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6540-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6540-136">CommonParameters</span></span>
<span data-ttu-id="f6540-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6540-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6540-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6540-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6540-139">입력</span><span class="sxs-lookup"><span data-stu-id="f6540-139">INPUTS</span></span>

### <span data-ttu-id="f6540-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f6540-140">System.String</span></span>

### <span data-ttu-id="f6540-141">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f6540-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f6540-142">출력</span><span class="sxs-lookup"><span data-stu-id="f6540-142">OUTPUTS</span></span>

### <span data-ttu-id="f6540-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f6540-143">System.String</span></span>

## <span data-ttu-id="f6540-144">상속자</span><span class="sxs-lookup"><span data-stu-id="f6540-144">NOTES</span></span>

## <span data-ttu-id="f6540-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6540-145">RELATED LINKS</span></span>

[<span data-ttu-id="f6540-146">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f6540-146">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f6540-147">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f6540-147">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="f6540-148">새로운 AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f6540-148">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f6540-149">제거-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f6540-149">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
