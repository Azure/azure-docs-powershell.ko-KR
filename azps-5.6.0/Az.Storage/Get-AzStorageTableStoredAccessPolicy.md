---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 2de23408aef9d9af4ebd23eb520261760883cf3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994784"
---
# <span data-ttu-id="ccc81-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ccc81-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="ccc81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccc81-102">SYNOPSIS</span></span>
<span data-ttu-id="ccc81-103">Azure Storage 테이블에 대한 저장된 액세스 정책 또는 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ccc81-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="ccc81-104">구문</span><span class="sxs-lookup"><span data-stu-id="ccc81-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccc81-105">설명</span><span class="sxs-lookup"><span data-stu-id="ccc81-105">DESCRIPTION</span></span>
<span data-ttu-id="ccc81-106">**Get-AzStorageTableStoredAccessPolicy** cmdlet은 Azure Storage 테이블에 대한 저장된 액세스 정책 또는 정책을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ccc81-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="ccc81-107">예제</span><span class="sxs-lookup"><span data-stu-id="ccc81-107">EXAMPLES</span></span>

### <span data-ttu-id="ccc81-108">예제 1: 저장소 테이블에 저장된 액세스 정책 사용</span><span class="sxs-lookup"><span data-stu-id="ccc81-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="ccc81-109">이 명령은 Table02라는 저장소 테이블에서 Policy50이라는 액세스 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ccc81-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="ccc81-110">예제 2: 저장소 테이블에 저장된 모든 액세스 정책 사용</span><span class="sxs-lookup"><span data-stu-id="ccc81-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="ccc81-111">이 명령은 Table02라는 테이블의 모든 액세스 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ccc81-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="ccc81-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ccc81-112">PARAMETERS</span></span>

### <span data-ttu-id="ccc81-113">-Context</span><span class="sxs-lookup"><span data-stu-id="ccc81-113">-Context</span></span>
<span data-ttu-id="ccc81-114">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ccc81-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ccc81-115">저장소 컨텍스트를 구하기 위해 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccc81-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ccc81-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccc81-116">-DefaultProfile</span></span>
<span data-ttu-id="ccc81-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ccc81-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccc81-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="ccc81-118">-Policy</span></span>
<span data-ttu-id="ccc81-119">이 SAS(공유 액세스 서명) 토큰에 대한 사용 권한을 포함하는 저장된 액세스 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ccc81-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccc81-120">-Table</span><span class="sxs-lookup"><span data-stu-id="ccc81-120">-Table</span></span>
<span data-ttu-id="ccc81-121">Azure Storage 테이블 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ccc81-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="ccc81-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccc81-122">CommonParameters</span></span>
<span data-ttu-id="ccc81-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ccc81-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccc81-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ccc81-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccc81-125">입력</span><span class="sxs-lookup"><span data-stu-id="ccc81-125">INPUTS</span></span>

### <span data-ttu-id="ccc81-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ccc81-126">System.String</span></span>

### <span data-ttu-id="ccc81-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ccc81-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ccc81-128">출력</span><span class="sxs-lookup"><span data-stu-id="ccc81-128">OUTPUTS</span></span>

### <span data-ttu-id="ccc81-129">Microsoft.WindowsAzure.Storage.Table.SharedAccesssTablePolicy</span><span class="sxs-lookup"><span data-stu-id="ccc81-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="ccc81-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ccc81-130">NOTES</span></span>

## <span data-ttu-id="ccc81-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ccc81-131">RELATED LINKS</span></span>

[<span data-ttu-id="ccc81-132">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ccc81-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="ccc81-133">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ccc81-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="ccc81-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ccc81-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="ccc81-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ccc81-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


