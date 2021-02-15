---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
ms.openlocfilehash: 17a7e32d0686e68b70f2129edfbb617661057218
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195732"
---
# <span data-ttu-id="b4101-101">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="b4101-101">New-AzStorageQueueSASToken</span></span>

## <span data-ttu-id="b4101-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4101-102">SYNOPSIS</span></span>
<span data-ttu-id="b4101-103">Azure 저장소 큐에 대한 공유 액세스 서명 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b4101-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="b4101-104">구문</span><span class="sxs-lookup"><span data-stu-id="b4101-104">SYNTAX</span></span>

### <span data-ttu-id="b4101-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="b4101-105">SasPolicy</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4101-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="b4101-106">SasPermission</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4101-107">설명</span><span class="sxs-lookup"><span data-stu-id="b4101-107">DESCRIPTION</span></span>
<span data-ttu-id="b4101-108">**New-AzStorageQueueSASToken** cmdlet은 Azure 저장소 큐에 대한 공유 액세스 서명 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b4101-108">The **New-AzStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="b4101-109">예제</span><span class="sxs-lookup"><span data-stu-id="b4101-109">EXAMPLES</span></span>

### <span data-ttu-id="b4101-110">예제 1: 모든 권한이 있는 큐 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="b4101-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="b4101-111">이 예제에서는 모든 권한이 있는 큐 SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b4101-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="b4101-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4101-112">PARAMETERS</span></span>

### <span data-ttu-id="b4101-113">-Context</span><span class="sxs-lookup"><span data-stu-id="b4101-113">-Context</span></span>
<span data-ttu-id="b4101-114">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b4101-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b4101-115">cmdlet을 사용하여 만들 New-AzStorageContext 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4101-115">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b4101-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4101-116">-DefaultProfile</span></span>
<span data-ttu-id="b4101-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4101-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4101-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b4101-118">-ExpiryTime</span></span>
<span data-ttu-id="b4101-119">공유 액세스 서명이 더 이상 유효하지 않은 경우를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b4101-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="b4101-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="b4101-120">-FullUri</span></span>
<span data-ttu-id="b4101-121">이 cmdlet이 전체 Blob URI 및 공유 액세스 서명 토큰을 반환하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b4101-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="b4101-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="b4101-122">-IPAddressOrRange</span></span>
<span data-ttu-id="b4101-123">요청을 수락할 IP 주소 또는 IP 주소 범위를 지정합니다(예: 168.1.5.65 또는 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="b4101-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="b4101-124">범위는 포괄적입니다.</span><span class="sxs-lookup"><span data-stu-id="b4101-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="b4101-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b4101-125">-Name</span></span>
<span data-ttu-id="b4101-126">Azure 저장소 큐 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b4101-126">Specifies an Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4101-127">-Permission</span><span class="sxs-lookup"><span data-stu-id="b4101-127">-Permission</span></span>
<span data-ttu-id="b4101-128">저장소 큐에 대한 권한을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b4101-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="b4101-129">이 문자열은 읽기, 쓰기 및 삭제와 같은 `rwd` 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="b4101-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4101-130">-Policy</span><span class="sxs-lookup"><span data-stu-id="b4101-130">-Policy</span></span>
<span data-ttu-id="b4101-131">Azure에 저장된 액세스 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b4101-131">Specifies an Azure stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4101-132">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b4101-132">-Protocol</span></span>
<span data-ttu-id="b4101-133">요청에 허용되는 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b4101-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="b4101-134">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="b4101-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="b4101-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="b4101-135">HttpsOnly</span></span>
* <span data-ttu-id="b4101-136">HttpsOrHttp 기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="b4101-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4101-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b4101-137">-StartTime</span></span>
<span data-ttu-id="b4101-138">공유 액세스 서명이 유효해지는 경우를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b4101-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="b4101-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4101-139">CommonParameters</span></span>
<span data-ttu-id="b4101-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b4101-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4101-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b4101-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4101-142">입력</span><span class="sxs-lookup"><span data-stu-id="b4101-142">INPUTS</span></span>

### <span data-ttu-id="b4101-143">System.String</span><span class="sxs-lookup"><span data-stu-id="b4101-143">System.String</span></span>

### <span data-ttu-id="b4101-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b4101-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b4101-145">출력</span><span class="sxs-lookup"><span data-stu-id="b4101-145">OUTPUTS</span></span>

### <span data-ttu-id="b4101-146">System.String</span><span class="sxs-lookup"><span data-stu-id="b4101-146">System.String</span></span>

## <span data-ttu-id="b4101-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b4101-147">NOTES</span></span>

## <span data-ttu-id="b4101-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4101-148">RELATED LINKS</span></span>
