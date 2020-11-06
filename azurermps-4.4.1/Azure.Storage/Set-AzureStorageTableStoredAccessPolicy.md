---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f4dfc77be9006229e2919dd1a4e0cdb1dd8c548e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531899"
---
# <span data-ttu-id="be31c-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="be31c-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="be31c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be31c-102">SYNOPSIS</span></span>
<span data-ttu-id="be31c-103">Azure storage 테이블에 대해 저장 된 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be31c-103">Sets the stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be31c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="be31c-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be31c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="be31c-105">DESCRIPTION</span></span>
<span data-ttu-id="be31c-106">**AzureStorageTableStoredAccessPolicy** Cmdlet은 Azure storage 테이블에 대해 저장 된 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be31c-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="be31c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="be31c-107">EXAMPLES</span></span>

### <span data-ttu-id="be31c-108">예제 1: 모든 권한이 있는 테이블에서 저장 된 액세스 정책 설정</span><span class="sxs-lookup"><span data-stu-id="be31c-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="be31c-109">이 명령은 MyTable 이라는 저장소 테이블에 대 한 Policy08 라는 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be31c-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="be31c-110">변수</span><span class="sxs-lookup"><span data-stu-id="be31c-110">PARAMETERS</span></span>

### <span data-ttu-id="be31c-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="be31c-111">-Context</span></span>
<span data-ttu-id="be31c-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be31c-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="be31c-113">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="be31c-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be31c-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="be31c-114">-ExpiryTime</span></span>
<span data-ttu-id="be31c-115">저장 된 액세스 정책이 만료 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be31c-115">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="be31c-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="be31c-116">-NoExpiryTime</span></span>
<span data-ttu-id="be31c-117">액세스 정책에 만료 날짜가 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="be31c-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="be31c-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="be31c-118">-NoStartTime</span></span>
<span data-ttu-id="be31c-119">시작 시간이 $Null 설정 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="be31c-119">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="be31c-120">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="be31c-120">-Permission</span></span>
<span data-ttu-id="be31c-121">저장 된 액세스 정책에서 저장소 테이블에 액세스 하는 데 필요한 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be31c-121">Specifies permissions in the stored access policy to access the storage table.</span></span>

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

### <span data-ttu-id="be31c-122">-정책</span><span class="sxs-lookup"><span data-stu-id="be31c-122">-Policy</span></span>
<span data-ttu-id="be31c-123">저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be31c-123">Specifies the name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be31c-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="be31c-124">-StartTime</span></span>
<span data-ttu-id="be31c-125">저장 된 액세스 정책이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be31c-125">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="be31c-126">-테이블</span><span class="sxs-lookup"><span data-stu-id="be31c-126">-Table</span></span>
<span data-ttu-id="be31c-127">Azure 저장소 테이블 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be31c-127">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be31c-128">-확인</span><span class="sxs-lookup"><span data-stu-id="be31c-128">-Confirm</span></span>
<span data-ttu-id="be31c-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="be31c-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be31c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be31c-130">-WhatIf</span></span>
<span data-ttu-id="be31c-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="be31c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be31c-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be31c-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be31c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be31c-133">CommonParameters</span></span>
<span data-ttu-id="be31c-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be31c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be31c-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be31c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be31c-136">입력</span><span class="sxs-lookup"><span data-stu-id="be31c-136">INPUTS</span></span>

### <span data-ttu-id="be31c-137">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="be31c-137">IStorageContext</span></span>

<span data-ttu-id="be31c-138">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="be31c-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="be31c-139">이름</span><span class="sxs-lookup"><span data-stu-id="be31c-139">String</span></span>

<span data-ttu-id="be31c-140">' Table ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="be31c-140">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="be31c-141">출력</span><span class="sxs-lookup"><span data-stu-id="be31c-141">OUTPUTS</span></span>

### <span data-ttu-id="be31c-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="be31c-142">System.String</span></span>

## <span data-ttu-id="be31c-143">상속자</span><span class="sxs-lookup"><span data-stu-id="be31c-143">NOTES</span></span>

## <span data-ttu-id="be31c-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be31c-144">RELATED LINKS</span></span>

[<span data-ttu-id="be31c-145">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="be31c-145">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="be31c-146">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="be31c-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="be31c-147">새로운 AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="be31c-147">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="be31c-148">제거-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="be31c-148">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
