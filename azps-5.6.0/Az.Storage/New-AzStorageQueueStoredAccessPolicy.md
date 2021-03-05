---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: f676f644cb69880a0b403a4e656ce9cb435b7c77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002384"
---
# <span data-ttu-id="689e6-101">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="689e6-101">New-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="689e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="689e6-102">SYNOPSIS</span></span>
<span data-ttu-id="689e6-103">Azure 저장소 큐에 대한 저장된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="689e6-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="689e6-104">구문</span><span class="sxs-lookup"><span data-stu-id="689e6-104">SYNTAX</span></span>

```
New-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="689e6-105">설명</span><span class="sxs-lookup"><span data-stu-id="689e6-105">DESCRIPTION</span></span>
<span data-ttu-id="689e6-106">**New-AzStorageQueueStoredAccessPolicy** cmdlet은 Azure 저장소 큐에 대한 저장된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="689e6-106">The **New-AzStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="689e6-107">예제</span><span class="sxs-lookup"><span data-stu-id="689e6-107">EXAMPLES</span></span>

### <span data-ttu-id="689e6-108">예제 1: 저장소 큐에 저장된 액세스 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="689e6-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="689e6-109">이 명령은 MyQueue라는 저장소 큐에 Policy01이라는 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="689e6-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="689e6-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="689e6-110">PARAMETERS</span></span>

### <span data-ttu-id="689e6-111">-Context</span><span class="sxs-lookup"><span data-stu-id="689e6-111">-Context</span></span>
<span data-ttu-id="689e6-112">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="689e6-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="689e6-113">저장소 컨텍스트를 구하기 위해 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="689e6-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="689e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="689e6-114">-DefaultProfile</span></span>
<span data-ttu-id="689e6-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="689e6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="689e6-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="689e6-116">-ExpiryTime</span></span>
<span data-ttu-id="689e6-117">저장된 액세스 정책이 유효하지 않은 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="689e6-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="689e6-118">-권한</span><span class="sxs-lookup"><span data-stu-id="689e6-118">-Permission</span></span>
<span data-ttu-id="689e6-119">저장소 큐에 액세스하기 위해 저장된 액세스 정책에서 권한을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="689e6-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="689e6-120">이 문자열은 읽기, 쓰기 및 삭제와 같은 `rwd` 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="689e6-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="689e6-121">-Policy</span><span class="sxs-lookup"><span data-stu-id="689e6-121">-Policy</span></span>
<span data-ttu-id="689e6-122">저장된 액세스 정책의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="689e6-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="689e6-123">-Queue</span><span class="sxs-lookup"><span data-stu-id="689e6-123">-Queue</span></span>
<span data-ttu-id="689e6-124">Azure Storage 큐 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="689e6-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="689e6-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="689e6-125">-StartTime</span></span>
<span data-ttu-id="689e6-126">저장된 액세스 정책이 유효한 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="689e6-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="689e6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="689e6-127">CommonParameters</span></span>
<span data-ttu-id="689e6-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="689e6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="689e6-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="689e6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="689e6-130">입력</span><span class="sxs-lookup"><span data-stu-id="689e6-130">INPUTS</span></span>

### <span data-ttu-id="689e6-131">System.String</span><span class="sxs-lookup"><span data-stu-id="689e6-131">System.String</span></span>

### <span data-ttu-id="689e6-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="689e6-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="689e6-133">출력</span><span class="sxs-lookup"><span data-stu-id="689e6-133">OUTPUTS</span></span>

### <span data-ttu-id="689e6-134">System.String</span><span class="sxs-lookup"><span data-stu-id="689e6-134">System.String</span></span>

## <span data-ttu-id="689e6-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="689e6-135">NOTES</span></span>

## <span data-ttu-id="689e6-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="689e6-136">RELATED LINKS</span></span>

[<span data-ttu-id="689e6-137">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="689e6-137">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="689e6-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="689e6-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="689e6-139">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="689e6-139">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="689e6-140">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="689e6-140">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)


