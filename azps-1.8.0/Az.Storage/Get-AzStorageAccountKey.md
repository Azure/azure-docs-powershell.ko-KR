---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 5deeae1bf3484b8649545ae6e379ace73422ade6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698684"
---
# <span data-ttu-id="90db7-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="90db7-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="90db7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90db7-102">SYNOPSIS</span></span>
<span data-ttu-id="90db7-103">Azure 저장소 계정의 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90db7-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="90db7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="90db7-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90db7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="90db7-105">DESCRIPTION</span></span>
<span data-ttu-id="90db7-106">**AzStorageAccountKey** Cmdlet은 Azure 저장소 계정의 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90db7-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="90db7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="90db7-107">EXAMPLES</span></span>

### <span data-ttu-id="90db7-108">예제 1: 저장소 계정의 선택 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="90db7-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="90db7-109">이 명령은 지정 된 Azure 저장소 계정에 대 한 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90db7-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="90db7-110">예제 2: 저장소 계정에 대 한 특정 선택 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="90db7-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

## <span data-ttu-id="90db7-111">변수</span><span class="sxs-lookup"><span data-stu-id="90db7-111">PARAMETERS</span></span>

### <span data-ttu-id="90db7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90db7-112">-DefaultProfile</span></span>
<span data-ttu-id="90db7-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90db7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90db7-114">-이름</span><span class="sxs-lookup"><span data-stu-id="90db7-114">-Name</span></span>
<span data-ttu-id="90db7-115">이 cmdlet에서 키를 가져오는 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90db7-115">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90db7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90db7-116">-ResourceGroupName</span></span>
<span data-ttu-id="90db7-117">저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90db7-117">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90db7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90db7-118">CommonParameters</span></span>
<span data-ttu-id="90db7-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="90db7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90db7-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90db7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90db7-121">입력</span><span class="sxs-lookup"><span data-stu-id="90db7-121">INPUTS</span></span>

### <span data-ttu-id="90db7-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="90db7-122">System.String</span></span>

## <span data-ttu-id="90db7-123">출력</span><span class="sxs-lookup"><span data-stu-id="90db7-123">OUTPUTS</span></span>

### <span data-ttu-id="90db7-124">StorageAccountKey를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="90db7-124">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="90db7-125">상속자</span><span class="sxs-lookup"><span data-stu-id="90db7-125">NOTES</span></span>

## <span data-ttu-id="90db7-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90db7-126">RELATED LINKS</span></span>

[<span data-ttu-id="90db7-127">새로운 AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="90db7-127">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


