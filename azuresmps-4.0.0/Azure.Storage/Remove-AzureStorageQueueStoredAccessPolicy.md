---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: ''
schema: 2.0.0
ms.openlocfilehash: 116dcc8967ab18d0b67cd3e4eeea91190c38930f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523908"
---
# <span data-ttu-id="cc46e-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cc46e-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="cc46e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc46e-102">SYNOPSIS</span></span>
<span data-ttu-id="cc46e-103">Azure 저장소 큐에서 저장 된 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc46e-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="cc46e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cc46e-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc46e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cc46e-105">DESCRIPTION</span></span>
<span data-ttu-id="cc46e-106">**AzureStorageQueueStoredAccessPolicy** Cmdlet은 Azure 저장소 큐에서 저장 된 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc46e-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="cc46e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cc46e-107">EXAMPLES</span></span>

### <span data-ttu-id="cc46e-108">예제 1: 저장소 큐에서 저장 된 액세스 정책 제거</span><span class="sxs-lookup"><span data-stu-id="cc46e-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="cc46e-109">이 명령은 MyQueue 이라는 저장소 큐에서 Policy04 라는 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc46e-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="cc46e-110">변수</span><span class="sxs-lookup"><span data-stu-id="cc46e-110">PARAMETERS</span></span>

### <span data-ttu-id="cc46e-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="cc46e-111">-Context</span></span>
<span data-ttu-id="cc46e-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc46e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cc46e-113">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc46e-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cc46e-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc46e-114">-PassThru</span></span>
<span data-ttu-id="cc46e-115">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cc46e-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="cc46e-116">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cc46e-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="cc46e-117">-정책</span><span class="sxs-lookup"><span data-stu-id="cc46e-117">-Policy</span></span>
<span data-ttu-id="cc46e-118">이 SA (공유 액세스 서명) 토큰에 대 한 사용 권한이 포함 된 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc46e-118">Specifies the stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="cc46e-119">-큐</span><span class="sxs-lookup"><span data-stu-id="cc46e-119">-Queue</span></span>
<span data-ttu-id="cc46e-120">Azure 저장소 큐 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc46e-120">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="cc46e-121">-확인</span><span class="sxs-lookup"><span data-stu-id="cc46e-121">-Confirm</span></span>
<span data-ttu-id="cc46e-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc46e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc46e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc46e-123">-WhatIf</span></span>
<span data-ttu-id="cc46e-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cc46e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc46e-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cc46e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc46e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc46e-126">CommonParameters</span></span>
<span data-ttu-id="cc46e-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc46e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc46e-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc46e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc46e-129">입력</span><span class="sxs-lookup"><span data-stu-id="cc46e-129">INPUTS</span></span>

## <span data-ttu-id="cc46e-130">출력</span><span class="sxs-lookup"><span data-stu-id="cc46e-130">OUTPUTS</span></span>

## <span data-ttu-id="cc46e-131">상속자</span><span class="sxs-lookup"><span data-stu-id="cc46e-131">NOTES</span></span>

## <span data-ttu-id="cc46e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc46e-132">RELATED LINKS</span></span>

[<span data-ttu-id="cc46e-133">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cc46e-133">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="cc46e-134">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="cc46e-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="cc46e-135">새로운 AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cc46e-135">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="cc46e-136">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cc46e-136">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
