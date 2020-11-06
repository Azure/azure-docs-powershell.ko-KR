---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3276a23869633238ebc6b84dfa01934e5ad9896
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523224"
---
# <span data-ttu-id="3ab26-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3ab26-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="3ab26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ab26-102">SYNOPSIS</span></span>
<span data-ttu-id="3ab26-103">Azure 저장소 테이블에서 저장 된 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab26-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="3ab26-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3ab26-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ab26-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3ab26-105">DESCRIPTION</span></span>
<span data-ttu-id="3ab26-106">**AzureStorageTableStoredAccessPolicy** Cmdlet은 Azure 저장소 테이블에서 저장 된 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab26-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="3ab26-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3ab26-107">EXAMPLES</span></span>

### <span data-ttu-id="3ab26-108">예제 1: 저장소 테이블에서 저장 된 액세스 정책 제거</span><span class="sxs-lookup"><span data-stu-id="3ab26-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="3ab26-109">이 명령은 MyTable 이라는 저장소 테이블에서 Policy05 이라는 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab26-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="3ab26-110">변수</span><span class="sxs-lookup"><span data-stu-id="3ab26-110">PARAMETERS</span></span>

### <span data-ttu-id="3ab26-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="3ab26-111">-Context</span></span>
<span data-ttu-id="3ab26-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab26-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3ab26-113">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab26-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3ab26-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ab26-114">-PassThru</span></span>
<span data-ttu-id="3ab26-115">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3ab26-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="3ab26-116">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ab26-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="3ab26-117">-정책</span><span class="sxs-lookup"><span data-stu-id="3ab26-117">-Policy</span></span>
<span data-ttu-id="3ab26-118">이 SAS 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab26-118">Specifies the stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="3ab26-119">-테이블</span><span class="sxs-lookup"><span data-stu-id="3ab26-119">-Table</span></span>
<span data-ttu-id="3ab26-120">Azure 테이블 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab26-120">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="3ab26-121">-확인</span><span class="sxs-lookup"><span data-stu-id="3ab26-121">-Confirm</span></span>
<span data-ttu-id="3ab26-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab26-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ab26-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ab26-123">-WhatIf</span></span>
<span data-ttu-id="3ab26-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3ab26-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ab26-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ab26-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ab26-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ab26-126">CommonParameters</span></span>
<span data-ttu-id="3ab26-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab26-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ab26-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ab26-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ab26-129">입력</span><span class="sxs-lookup"><span data-stu-id="3ab26-129">INPUTS</span></span>

## <span data-ttu-id="3ab26-130">출력</span><span class="sxs-lookup"><span data-stu-id="3ab26-130">OUTPUTS</span></span>

## <span data-ttu-id="3ab26-131">상속자</span><span class="sxs-lookup"><span data-stu-id="3ab26-131">NOTES</span></span>

## <span data-ttu-id="3ab26-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ab26-132">RELATED LINKS</span></span>

[<span data-ttu-id="3ab26-133">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3ab26-133">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3ab26-134">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3ab26-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="3ab26-135">새로운 AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3ab26-135">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3ab26-136">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3ab26-136">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
