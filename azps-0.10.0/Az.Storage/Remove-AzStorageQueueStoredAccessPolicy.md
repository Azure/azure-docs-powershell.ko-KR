---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 74189f488519c903e8e02b1e86585d03a9e80446
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876220"
---
# <span data-ttu-id="4930e-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4930e-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="4930e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4930e-102">SYNOPSIS</span></span>
<span data-ttu-id="4930e-103">Azure 저장소 큐에서 저장 된 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4930e-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="4930e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4930e-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4930e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4930e-105">DESCRIPTION</span></span>
<span data-ttu-id="4930e-106">**AzStorageQueueStoredAccessPolicy** Cmdlet은 Azure 저장소 큐에서 저장 된 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4930e-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="4930e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4930e-107">EXAMPLES</span></span>

### <span data-ttu-id="4930e-108">예제 1: 저장소 큐에서 저장 된 액세스 정책 제거</span><span class="sxs-lookup"><span data-stu-id="4930e-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="4930e-109">이 명령은 MyQueue 이라는 저장소 큐에서 Policy04 라는 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4930e-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="4930e-110">변수</span><span class="sxs-lookup"><span data-stu-id="4930e-110">PARAMETERS</span></span>

### <span data-ttu-id="4930e-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="4930e-111">-Context</span></span>
<span data-ttu-id="4930e-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4930e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4930e-113">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4930e-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4930e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4930e-114">-DefaultProfile</span></span>
<span data-ttu-id="4930e-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4930e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4930e-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4930e-116">-PassThru</span></span>
<span data-ttu-id="4930e-117">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4930e-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="4930e-118">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4930e-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4930e-119">-정책</span><span class="sxs-lookup"><span data-stu-id="4930e-119">-Policy</span></span>
<span data-ttu-id="4930e-120">이 cmdlet이 제거 하는 저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4930e-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4930e-121">-큐</span><span class="sxs-lookup"><span data-stu-id="4930e-121">-Queue</span></span>
<span data-ttu-id="4930e-122">Azure 저장소 큐 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4930e-122">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4930e-123">-확인</span><span class="sxs-lookup"><span data-stu-id="4930e-123">-Confirm</span></span>
<span data-ttu-id="4930e-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4930e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4930e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4930e-125">-WhatIf</span></span>
<span data-ttu-id="4930e-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4930e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4930e-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4930e-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4930e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4930e-128">CommonParameters</span></span>
<span data-ttu-id="4930e-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4930e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4930e-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4930e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4930e-131">입력</span><span class="sxs-lookup"><span data-stu-id="4930e-131">INPUTS</span></span>

### <span data-ttu-id="4930e-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4930e-132">System.String</span></span>

### <span data-ttu-id="4930e-133">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4930e-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4930e-134">출력</span><span class="sxs-lookup"><span data-stu-id="4930e-134">OUTPUTS</span></span>

### <span data-ttu-id="4930e-135">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="4930e-135">System.Boolean</span></span>

## <span data-ttu-id="4930e-136">상속자</span><span class="sxs-lookup"><span data-stu-id="4930e-136">NOTES</span></span>

## <span data-ttu-id="4930e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4930e-137">RELATED LINKS</span></span>

[<span data-ttu-id="4930e-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4930e-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4930e-139">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4930e-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="4930e-140">새로운 AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4930e-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4930e-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4930e-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
