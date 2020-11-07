---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: ba81e987e19d6698c8ea1d9e489d353d58007aea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698686"
---
# <span data-ttu-id="39891-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39891-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="39891-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39891-102">SYNOPSIS</span></span>
<span data-ttu-id="39891-103">저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="39891-103">Gets a Storage account.</span></span>

## <span data-ttu-id="39891-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39891-104">SYNTAX</span></span>

### <span data-ttu-id="39891-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="39891-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="39891-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="39891-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39891-107">설명은</span><span class="sxs-lookup"><span data-stu-id="39891-107">DESCRIPTION</span></span>
<span data-ttu-id="39891-108">**AzStorageAccount** cmdlet은 지정 된 저장소 계정 또는 리소스 그룹 또는 구독에 있는 모든 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="39891-108">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="39891-109">예제의</span><span class="sxs-lookup"><span data-stu-id="39891-109">EXAMPLES</span></span>

### <span data-ttu-id="39891-110">예제 1: 지정 된 저장소 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="39891-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="39891-111">이 명령은 지정 된 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="39891-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="39891-112">예제 2: 리소스 그룹의 모든 저장소 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="39891-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="39891-113">이 명령은 리소스 그룹의 모든 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="39891-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="39891-114">예제 3: 구독에서 모든 저장소 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="39891-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="39891-115">이 명령은 구독에 있는 모든 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="39891-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="39891-116">변수</span><span class="sxs-lookup"><span data-stu-id="39891-116">PARAMETERS</span></span>

### <span data-ttu-id="39891-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39891-117">-DefaultProfile</span></span>
<span data-ttu-id="39891-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39891-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39891-119">-이름</span><span class="sxs-lookup"><span data-stu-id="39891-119">-Name</span></span>
<span data-ttu-id="39891-120">가져올 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39891-120">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="39891-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39891-121">-ResourceGroupName</span></span>
<span data-ttu-id="39891-122">가져올 저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39891-122">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="39891-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39891-123">CommonParameters</span></span>
<span data-ttu-id="39891-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39891-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39891-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39891-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39891-126">입력</span><span class="sxs-lookup"><span data-stu-id="39891-126">INPUTS</span></span>

### <span data-ttu-id="39891-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="39891-127">System.String</span></span>

## <span data-ttu-id="39891-128">출력</span><span class="sxs-lookup"><span data-stu-id="39891-128">OUTPUTS</span></span>

### <span data-ttu-id="39891-129">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39891-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="39891-130">상속자</span><span class="sxs-lookup"><span data-stu-id="39891-130">NOTES</span></span>

## <span data-ttu-id="39891-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39891-131">RELATED LINKS</span></span>

[<span data-ttu-id="39891-132">새로운 AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39891-132">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="39891-133">제거-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39891-133">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="39891-134">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39891-134">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


