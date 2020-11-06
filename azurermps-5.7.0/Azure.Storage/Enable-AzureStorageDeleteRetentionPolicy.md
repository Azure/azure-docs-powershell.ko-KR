---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/enable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: f8303a9d87a2bd5312732bd01eb3d42bd1e0a285
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527175"
---
# <span data-ttu-id="37dfa-101">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="37dfa-101">Enable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="37dfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="37dfa-103">Azure 저장소 Blob 서비스에 대 한 삭제 보존 정책을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37dfa-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37dfa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="37dfa-104">SYNTAX</span></span>

```
Enable-AzureStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37dfa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="37dfa-105">DESCRIPTION</span></span>
<span data-ttu-id="37dfa-106">AzureStorageDeleteRetentionPolicy cmdlet을 **사용** 하면 Azure 저장소 Blob 서비스에 대 한 삭제 보존 정책을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37dfa-106">The **Enable-AzureStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="37dfa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="37dfa-107">EXAMPLES</span></span>

### <span data-ttu-id="37dfa-108">예제 1: Blob 서비스에 대 한 삭제 보존 정책 사용</span><span class="sxs-lookup"><span data-stu-id="37dfa-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzureStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="37dfa-109">이 명령은 Blob 서비스에 대 한 삭제 보존 정책을 활성화 하 고 삭제 된 blob 보존 일을 3으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37dfa-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="37dfa-110">변수</span><span class="sxs-lookup"><span data-stu-id="37dfa-110">PARAMETERS</span></span>

### <span data-ttu-id="37dfa-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="37dfa-111">-Context</span></span>
<span data-ttu-id="37dfa-112">Azure 저장소 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="37dfa-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="37dfa-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37dfa-113">-PassThru</span></span>
<span data-ttu-id="37dfa-114">DeleteRetentionPolicyProperties 표시</span><span class="sxs-lookup"><span data-stu-id="37dfa-114">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="37dfa-115">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="37dfa-115">-RetentionDays</span></span>
<span data-ttu-id="37dfa-116">DeleteRetentionPolicy 보존 일 수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37dfa-116">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37dfa-117">-확인</span><span class="sxs-lookup"><span data-stu-id="37dfa-117">-Confirm</span></span>
<span data-ttu-id="37dfa-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="37dfa-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37dfa-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37dfa-119">-WhatIf</span></span>
<span data-ttu-id="37dfa-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="37dfa-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37dfa-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37dfa-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37dfa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37dfa-122">CommonParameters</span></span>
<span data-ttu-id="37dfa-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37dfa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37dfa-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37dfa-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37dfa-125">입력</span><span class="sxs-lookup"><span data-stu-id="37dfa-125">INPUTS</span></span>

### <span data-ttu-id="37dfa-126">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="37dfa-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="37dfa-127">출력</span><span class="sxs-lookup"><span data-stu-id="37dfa-127">OUTPUTS</span></span>

### <span data-ttu-id="37dfa-128">WindowsAzure. DeleteRetentionPolicyProperties를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="37dfa-128">Microsoft.WindowsAzure.Storage.Shared.Protocol.DeleteRetentionPolicyProperties</span></span>

## <span data-ttu-id="37dfa-129">상속자</span><span class="sxs-lookup"><span data-stu-id="37dfa-129">NOTES</span></span>

## <span data-ttu-id="37dfa-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37dfa-130">RELATED LINKS</span></span>

