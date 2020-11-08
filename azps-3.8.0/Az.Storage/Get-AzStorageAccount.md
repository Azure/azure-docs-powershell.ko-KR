---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: db0c0672a6f60aa8c46f85a98e74f5184842cd72
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042299"
---
# <span data-ttu-id="9ad4f-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9ad4f-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="9ad4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ad4f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad4f-103">저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ad4f-103">Gets a Storage account.</span></span>

## <span data-ttu-id="9ad4f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ad4f-104">SYNTAX</span></span>

### <span data-ttu-id="9ad4f-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad4f-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ad4f-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad4f-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ad4f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9ad4f-107">DESCRIPTION</span></span>
<span data-ttu-id="9ad4f-108">**AzStorageAccount** cmdlet은 지정 된 저장소 계정 또는 리소스 그룹 또는 구독에 있는 모든 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ad4f-108">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="9ad4f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9ad4f-109">EXAMPLES</span></span>

### <span data-ttu-id="9ad4f-110">예제 1: 지정 된 저장소 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="9ad4f-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="9ad4f-111">이 명령은 지정 된 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ad4f-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="9ad4f-112">예제 2: 리소스 그룹의 모든 저장소 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="9ad4f-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="9ad4f-113">이 명령은 리소스 그룹의 모든 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ad4f-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="9ad4f-114">예제 3: 구독에서 모든 저장소 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="9ad4f-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="9ad4f-115">이 명령은 구독에 있는 모든 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ad4f-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="9ad4f-116">변수</span><span class="sxs-lookup"><span data-stu-id="9ad4f-116">PARAMETERS</span></span>

### <span data-ttu-id="9ad4f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad4f-117">-DefaultProfile</span></span>
<span data-ttu-id="9ad4f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ad4f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ad4f-119">-IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="9ad4f-119">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="9ad4f-120">저장소 계정의 GeoReplicationStats를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ad4f-120">Get the GeoReplicationStats of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ad4f-121">-이름</span><span class="sxs-lookup"><span data-stu-id="9ad4f-121">-Name</span></span>
<span data-ttu-id="9ad4f-122">가져올 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ad4f-122">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ad4f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ad4f-123">-ResourceGroupName</span></span>
<span data-ttu-id="9ad4f-124">가져올 저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ad4f-124">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ad4f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad4f-125">CommonParameters</span></span>
<span data-ttu-id="9ad4f-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ad4f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad4f-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ad4f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad4f-128">입력</span><span class="sxs-lookup"><span data-stu-id="9ad4f-128">INPUTS</span></span>

### <span data-ttu-id="9ad4f-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9ad4f-129">System.String</span></span>

## <span data-ttu-id="9ad4f-130">출력</span><span class="sxs-lookup"><span data-stu-id="9ad4f-130">OUTPUTS</span></span>

### <span data-ttu-id="9ad4f-131">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9ad4f-131">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="9ad4f-132">상속자</span><span class="sxs-lookup"><span data-stu-id="9ad4f-132">NOTES</span></span>

## <span data-ttu-id="9ad4f-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ad4f-133">RELATED LINKS</span></span>

[<span data-ttu-id="9ad4f-134">새로운 AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9ad4f-134">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="9ad4f-135">제거-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9ad4f-135">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="9ad4f-136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9ad4f-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


