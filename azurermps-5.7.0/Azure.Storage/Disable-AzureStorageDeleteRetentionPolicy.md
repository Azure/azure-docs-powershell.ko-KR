---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: d3de0cc49eb0e36572daa9e4cfbbb41c0db0936a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702182"
---
# <span data-ttu-id="dc454-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dc454-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="dc454-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc454-102">SYNOPSIS</span></span>
<span data-ttu-id="dc454-103">Azure 저장소 Blob 서비스에 대해 보존 정책 삭제를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc454-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc454-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dc454-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc454-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dc454-105">DESCRIPTION</span></span>
<span data-ttu-id="dc454-106">**AzureStorageDeleteRetentionPolicy** Cmdlet은 Azure Storage Blob service에 대 한 삭제 보존 정책을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc454-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="dc454-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dc454-107">EXAMPLES</span></span>

### <span data-ttu-id="dc454-108">예제 1: Blob 서비스에 대 한 삭제 보존 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="dc454-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="dc454-109">이 명령은 Blob 서비스에 대 한 삭제 보존 정책을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc454-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="dc454-110">변수</span><span class="sxs-lookup"><span data-stu-id="dc454-110">PARAMETERS</span></span>

### <span data-ttu-id="dc454-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="dc454-111">-Context</span></span>
<span data-ttu-id="dc454-112">Azure 저장소 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="dc454-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="dc454-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc454-113">-PassThru</span></span>
<span data-ttu-id="dc454-114">DeleteRetentionPolicyProperties 표시</span><span class="sxs-lookup"><span data-stu-id="dc454-114">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="dc454-115">-확인</span><span class="sxs-lookup"><span data-stu-id="dc454-115">-Confirm</span></span>
<span data-ttu-id="dc454-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc454-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc454-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc454-117">-WhatIf</span></span>
<span data-ttu-id="dc454-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dc454-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc454-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc454-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc454-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc454-120">CommonParameters</span></span>
<span data-ttu-id="dc454-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc454-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc454-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc454-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc454-123">입력</span><span class="sxs-lookup"><span data-stu-id="dc454-123">INPUTS</span></span>

### <span data-ttu-id="dc454-124">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dc454-124">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dc454-125">출력</span><span class="sxs-lookup"><span data-stu-id="dc454-125">OUTPUTS</span></span>

### <span data-ttu-id="dc454-126">WindowsAzure. PSSeriviceProperties를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc454-126">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceMode.PSSeriviceProperties</span></span>

## <span data-ttu-id="dc454-127">상속자</span><span class="sxs-lookup"><span data-stu-id="dc454-127">NOTES</span></span>

## <span data-ttu-id="dc454-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc454-128">RELATED LINKS</span></span>

