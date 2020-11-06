---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 7ee384fb26ed8e16b377800fc7e3912f33b81669
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528364"
---
# <span data-ttu-id="7baf3-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7baf3-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="7baf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7baf3-102">SYNOPSIS</span></span>
<span data-ttu-id="7baf3-103">Azure 저장소 테이블에서 저장 된 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7baf3-103">Removes a stored access policy from an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7baf3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7baf3-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7baf3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7baf3-105">DESCRIPTION</span></span>
<span data-ttu-id="7baf3-106">**AzureStorageTableStoredAccessPolicy** Cmdlet은 Azure 저장소 테이블에서 저장 된 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7baf3-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="7baf3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7baf3-107">EXAMPLES</span></span>

### <span data-ttu-id="7baf3-108">예제 1: 저장소 테이블에서 저장 된 액세스 정책 제거</span><span class="sxs-lookup"><span data-stu-id="7baf3-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="7baf3-109">이 명령은 MyTable 이라는 저장소 테이블에서 Policy05 이라는 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7baf3-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="7baf3-110">변수</span><span class="sxs-lookup"><span data-stu-id="7baf3-110">PARAMETERS</span></span>

### <span data-ttu-id="7baf3-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="7baf3-111">-Context</span></span>
<span data-ttu-id="7baf3-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7baf3-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7baf3-113">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7baf3-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7baf3-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7baf3-114">-PassThru</span></span>
<span data-ttu-id="7baf3-115">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7baf3-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="7baf3-116">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7baf3-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="7baf3-117">-정책</span><span class="sxs-lookup"><span data-stu-id="7baf3-117">-Policy</span></span>
<span data-ttu-id="7baf3-118">이 cmdlet이 제거 하는 저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7baf3-118">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7baf3-119">-테이블</span><span class="sxs-lookup"><span data-stu-id="7baf3-119">-Table</span></span>
<span data-ttu-id="7baf3-120">Azure 테이블 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7baf3-120">Specifies the Azure table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7baf3-121">-확인</span><span class="sxs-lookup"><span data-stu-id="7baf3-121">-Confirm</span></span>
<span data-ttu-id="7baf3-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7baf3-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7baf3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7baf3-123">-WhatIf</span></span>
<span data-ttu-id="7baf3-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7baf3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7baf3-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7baf3-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7baf3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7baf3-126">CommonParameters</span></span>
<span data-ttu-id="7baf3-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7baf3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7baf3-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7baf3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7baf3-129">입력</span><span class="sxs-lookup"><span data-stu-id="7baf3-129">INPUTS</span></span>

### <span data-ttu-id="7baf3-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7baf3-130">IStorageContext</span></span>

<span data-ttu-id="7baf3-131">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7baf3-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="7baf3-132">출력</span><span class="sxs-lookup"><span data-stu-id="7baf3-132">OUTPUTS</span></span>

### <span data-ttu-id="7baf3-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7baf3-133">System.Boolean</span></span>

## <span data-ttu-id="7baf3-134">상속자</span><span class="sxs-lookup"><span data-stu-id="7baf3-134">NOTES</span></span>

## <span data-ttu-id="7baf3-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7baf3-135">RELATED LINKS</span></span>

[<span data-ttu-id="7baf3-136">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7baf3-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="7baf3-137">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7baf3-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="7baf3-138">새로운 AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7baf3-138">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="7baf3-139">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7baf3-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
