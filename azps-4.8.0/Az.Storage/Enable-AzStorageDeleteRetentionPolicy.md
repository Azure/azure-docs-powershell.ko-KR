---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 36176b16fab75b24549ceeb3d107114632703129
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056909"
---
# <span data-ttu-id="2dded-101">Enable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2dded-101">Enable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="2dded-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dded-102">SYNOPSIS</span></span>
<span data-ttu-id="2dded-103">Azure 저장소 Blob 서비스에 대 한 삭제 보존 정책을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dded-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="2dded-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2dded-104">SYNTAX</span></span>

```
Enable-AzStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dded-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2dded-105">DESCRIPTION</span></span>
<span data-ttu-id="2dded-106">AzStorageDeleteRetentionPolicy cmdlet을 **사용** 하면 Azure 저장소 Blob 서비스에 대 한 삭제 보존 정책을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2dded-106">The **Enable-AzStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="2dded-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2dded-107">EXAMPLES</span></span>

### <span data-ttu-id="2dded-108">예제 1: Blob 서비스에 대 한 삭제 보존 정책 사용</span><span class="sxs-lookup"><span data-stu-id="2dded-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="2dded-109">이 명령은 Blob 서비스에 대 한 삭제 보존 정책을 활성화 하 고 삭제 된 blob 보존 일을 3으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dded-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="2dded-110">변수</span><span class="sxs-lookup"><span data-stu-id="2dded-110">PARAMETERS</span></span>

### <span data-ttu-id="2dded-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="2dded-111">-Context</span></span>
<span data-ttu-id="2dded-112">Azure 저장소 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="2dded-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="2dded-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dded-113">-DefaultProfile</span></span>
<span data-ttu-id="2dded-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2dded-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dded-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2dded-115">-PassThru</span></span>
<span data-ttu-id="2dded-116">DeleteRetentionPolicyProperties 표시</span><span class="sxs-lookup"><span data-stu-id="2dded-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="2dded-117">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="2dded-117">-RetentionDays</span></span>
<span data-ttu-id="2dded-118">DeleteRetentionPolicy 보존 일 수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dded-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dded-119">-확인</span><span class="sxs-lookup"><span data-stu-id="2dded-119">-Confirm</span></span>
<span data-ttu-id="2dded-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dded-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dded-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dded-121">-WhatIf</span></span>
<span data-ttu-id="2dded-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2dded-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dded-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2dded-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dded-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dded-124">CommonParameters</span></span>
<span data-ttu-id="2dded-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dded-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dded-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dded-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dded-127">입력</span><span class="sxs-lookup"><span data-stu-id="2dded-127">INPUTS</span></span>

### <span data-ttu-id="2dded-128">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2dded-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2dded-129">출력</span><span class="sxs-lookup"><span data-stu-id="2dded-129">OUTPUTS</span></span>

### <span data-ttu-id="2dded-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2dded-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="2dded-131">상속자</span><span class="sxs-lookup"><span data-stu-id="2dded-131">NOTES</span></span>

## <span data-ttu-id="2dded-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2dded-132">RELATED LINKS</span></span>
