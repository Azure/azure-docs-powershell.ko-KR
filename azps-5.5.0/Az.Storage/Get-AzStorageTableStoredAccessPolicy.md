---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: b17a294392ca4336d4a96e5d136ad4e321eb45a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190884"
---
# <span data-ttu-id="b78e2-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b78e2-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="b78e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b78e2-102">SYNOPSIS</span></span>
<span data-ttu-id="b78e2-103">Azure 저장소 테이블에 대한 저장된 액세스 정책 또는 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b78e2-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="b78e2-104">구문</span><span class="sxs-lookup"><span data-stu-id="b78e2-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b78e2-105">설명</span><span class="sxs-lookup"><span data-stu-id="b78e2-105">DESCRIPTION</span></span>
<span data-ttu-id="b78e2-106">**Get-AzStorageTableStoredAccessPolicy** cmdlet은 Azure 저장소 테이블에 대한 저장된 액세스 정책 또는 정책을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b78e2-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="b78e2-107">예제</span><span class="sxs-lookup"><span data-stu-id="b78e2-107">EXAMPLES</span></span>

### <span data-ttu-id="b78e2-108">예제 1: 저장소 테이블에 저장된 액세스 정책 얻기</span><span class="sxs-lookup"><span data-stu-id="b78e2-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="b78e2-109">이 명령은 Table02라는 저장소 테이블에서 Policy50이라는 액세스 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b78e2-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="b78e2-110">예제 2: 저장소 테이블에 저장된 모든 액세스 정책 얻기</span><span class="sxs-lookup"><span data-stu-id="b78e2-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="b78e2-111">이 명령은 Table02라는 테이블의 모든 액세스 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b78e2-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="b78e2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b78e2-112">PARAMETERS</span></span>

### <span data-ttu-id="b78e2-113">-Context</span><span class="sxs-lookup"><span data-stu-id="b78e2-113">-Context</span></span>
<span data-ttu-id="b78e2-114">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b78e2-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b78e2-115">저장소 컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b78e2-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b78e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b78e2-116">-DefaultProfile</span></span>
<span data-ttu-id="b78e2-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b78e2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b78e2-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="b78e2-118">-Policy</span></span>
<span data-ttu-id="b78e2-119">이 SAS(공유 액세스 서명) 토큰에 대한 사용 권한을 포함하는 저장된 액세스 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b78e2-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="b78e2-120">-Table</span><span class="sxs-lookup"><span data-stu-id="b78e2-120">-Table</span></span>
<span data-ttu-id="b78e2-121">Azure 저장소 테이블 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b78e2-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="b78e2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b78e2-122">CommonParameters</span></span>
<span data-ttu-id="b78e2-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b78e2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b78e2-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b78e2-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b78e2-125">입력</span><span class="sxs-lookup"><span data-stu-id="b78e2-125">INPUTS</span></span>

### <span data-ttu-id="b78e2-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b78e2-126">System.String</span></span>

### <span data-ttu-id="b78e2-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b78e2-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b78e2-128">출력</span><span class="sxs-lookup"><span data-stu-id="b78e2-128">OUTPUTS</span></span>

### <span data-ttu-id="b78e2-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="b78e2-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="b78e2-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b78e2-130">NOTES</span></span>

## <span data-ttu-id="b78e2-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b78e2-131">RELATED LINKS</span></span>

[<span data-ttu-id="b78e2-132">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b78e2-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b78e2-133">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b78e2-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b78e2-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b78e2-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b78e2-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b78e2-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


