---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 1d55c52b3c022e9e935051cdb1ad23aae32eecbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973355"
---
# <span data-ttu-id="bd31e-101">Enable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bd31e-101">Enable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="bd31e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd31e-102">SYNOPSIS</span></span>
<span data-ttu-id="bd31e-103">Azure Storage Blob 서비스에 대한 삭제 보존 정책을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd31e-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="bd31e-104">구문</span><span class="sxs-lookup"><span data-stu-id="bd31e-104">SYNTAX</span></span>

```
Enable-AzStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd31e-105">설명</span><span class="sxs-lookup"><span data-stu-id="bd31e-105">DESCRIPTION</span></span>
<span data-ttu-id="bd31e-106">**Enable-AzStorageDeleteRetentionPolicy** cmdlet을 사용하면 Azure Storage Blob 서비스에 대한 삭제 보존 정책을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd31e-106">The **Enable-AzStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="bd31e-107">예제</span><span class="sxs-lookup"><span data-stu-id="bd31e-107">EXAMPLES</span></span>

### <span data-ttu-id="bd31e-108">예제 1: Blob 서비스에 대한 삭제 보존 정책 사용</span><span class="sxs-lookup"><span data-stu-id="bd31e-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="bd31e-109">이 명령을 사용하면 Blob 서비스에 대한 삭제 보존 정책을 사용할 수 있으며 삭제된 Blob 보존 일 수를 3으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd31e-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="bd31e-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bd31e-110">PARAMETERS</span></span>

### <span data-ttu-id="bd31e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="bd31e-111">-Context</span></span>
<span data-ttu-id="bd31e-112">Azure Storage 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="bd31e-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="bd31e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd31e-113">-DefaultProfile</span></span>
<span data-ttu-id="bd31e-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bd31e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd31e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd31e-115">-PassThru</span></span>
<span data-ttu-id="bd31e-116">Display DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="bd31e-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="bd31e-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="bd31e-117">-RetentionDays</span></span>
<span data-ttu-id="bd31e-118">DeleteRetentionPolicy에 대한 보존 일 수를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd31e-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="bd31e-119">-확인</span><span class="sxs-lookup"><span data-stu-id="bd31e-119">-Confirm</span></span>
<span data-ttu-id="bd31e-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd31e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd31e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd31e-121">-WhatIf</span></span>
<span data-ttu-id="bd31e-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bd31e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd31e-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd31e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd31e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd31e-124">CommonParameters</span></span>
<span data-ttu-id="bd31e-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bd31e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd31e-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bd31e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd31e-127">입력</span><span class="sxs-lookup"><span data-stu-id="bd31e-127">INPUTS</span></span>

### <span data-ttu-id="bd31e-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bd31e-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bd31e-129">출력</span><span class="sxs-lookup"><span data-stu-id="bd31e-129">OUTPUTS</span></span>

### <span data-ttu-id="bd31e-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bd31e-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="bd31e-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bd31e-131">NOTES</span></span>

## <span data-ttu-id="bd31e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd31e-132">RELATED LINKS</span></span>
