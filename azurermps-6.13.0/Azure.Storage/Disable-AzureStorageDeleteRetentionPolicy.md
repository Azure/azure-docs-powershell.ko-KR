---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 656fe09054b1cfae90175cc4ea55370f80dfd8e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526456"
---
# <span data-ttu-id="dfc2a-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dfc2a-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="dfc2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfc2a-102">SYNOPSIS</span></span>
<span data-ttu-id="dfc2a-103">Azure 저장소 Blob 서비스에 대해 보존 정책 삭제를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc2a-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfc2a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dfc2a-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfc2a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dfc2a-105">DESCRIPTION</span></span>
<span data-ttu-id="dfc2a-106">**AzureStorageDeleteRetentionPolicy** Cmdlet은 Azure Storage Blob service에 대 한 삭제 보존 정책을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc2a-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="dfc2a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dfc2a-107">EXAMPLES</span></span>

### <span data-ttu-id="dfc2a-108">예제 1: Blob 서비스에 대 한 삭제 보존 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="dfc2a-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="dfc2a-109">이 명령은 Blob 서비스에 대 한 삭제 보존 정책을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc2a-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="dfc2a-110">변수</span><span class="sxs-lookup"><span data-stu-id="dfc2a-110">PARAMETERS</span></span>

### <span data-ttu-id="dfc2a-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="dfc2a-111">-Context</span></span>
<span data-ttu-id="dfc2a-112">Azure 저장소 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="dfc2a-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="dfc2a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfc2a-113">-DefaultProfile</span></span>
<span data-ttu-id="dfc2a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dfc2a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfc2a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dfc2a-115">-PassThru</span></span>
<span data-ttu-id="dfc2a-116">DeleteRetentionPolicyProperties 표시</span><span class="sxs-lookup"><span data-stu-id="dfc2a-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="dfc2a-117">-확인</span><span class="sxs-lookup"><span data-stu-id="dfc2a-117">-Confirm</span></span>
<span data-ttu-id="dfc2a-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc2a-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfc2a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfc2a-119">-WhatIf</span></span>
<span data-ttu-id="dfc2a-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dfc2a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfc2a-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc2a-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfc2a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfc2a-122">CommonParameters</span></span>
<span data-ttu-id="dfc2a-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc2a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfc2a-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfc2a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfc2a-125">입력</span><span class="sxs-lookup"><span data-stu-id="dfc2a-125">INPUTS</span></span>

### <span data-ttu-id="dfc2a-126">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dfc2a-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dfc2a-127">출력</span><span class="sxs-lookup"><span data-stu-id="dfc2a-127">OUTPUTS</span></span>

### <span data-ttu-id="dfc2a-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dfc2a-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="dfc2a-129">상속자</span><span class="sxs-lookup"><span data-stu-id="dfc2a-129">NOTES</span></span>

## <span data-ttu-id="dfc2a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfc2a-130">RELATED LINKS</span></span>
