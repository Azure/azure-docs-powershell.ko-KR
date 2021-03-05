---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: 12881d387d1e98bef8ca1fa00790b0332a338b7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973387"
---
# <span data-ttu-id="b3985-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b3985-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="b3985-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3985-102">SYNOPSIS</span></span>
<span data-ttu-id="b3985-103">Azure Storage 계정에 대한 정적 웹 사이트를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b3985-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="b3985-104">구문</span><span class="sxs-lookup"><span data-stu-id="b3985-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3985-105">설명</span><span class="sxs-lookup"><span data-stu-id="b3985-105">DESCRIPTION</span></span>
<span data-ttu-id="b3985-106">**Disable-AzStorageStaticWebsite** cmdlet은 Azure Storage 계정에 대한 정적 웹 사이트를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b3985-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="b3985-107">예제</span><span class="sxs-lookup"><span data-stu-id="b3985-107">EXAMPLES</span></span>

### <span data-ttu-id="b3985-108">예제 1: Azure Storage 계정에 대한 정적 웹 사이트 사용 안 하세요.</span><span class="sxs-lookup"><span data-stu-id="b3985-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="b3985-109">이 명령은 Azure Storage 계정에 대한 정적 웹 사이트를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b3985-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="b3985-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b3985-110">PARAMETERS</span></span>

### <span data-ttu-id="b3985-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b3985-111">-Context</span></span>
<span data-ttu-id="b3985-112">Azure Storage 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="b3985-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="b3985-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3985-113">-DefaultProfile</span></span>
<span data-ttu-id="b3985-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3985-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3985-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3985-115">-PassThru</span></span>
<span data-ttu-id="b3985-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b3985-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b3985-117">-확인</span><span class="sxs-lookup"><span data-stu-id="b3985-117">-Confirm</span></span>
<span data-ttu-id="b3985-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3985-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3985-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3985-119">-WhatIf</span></span>
<span data-ttu-id="b3985-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b3985-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3985-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3985-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3985-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3985-122">CommonParameters</span></span>
<span data-ttu-id="b3985-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b3985-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3985-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b3985-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3985-125">입력</span><span class="sxs-lookup"><span data-stu-id="b3985-125">INPUTS</span></span>

### <span data-ttu-id="b3985-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b3985-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b3985-127">출력</span><span class="sxs-lookup"><span data-stu-id="b3985-127">OUTPUTS</span></span>

### <span data-ttu-id="b3985-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="b3985-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="b3985-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b3985-129">NOTES</span></span>

## <span data-ttu-id="b3985-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3985-130">RELATED LINKS</span></span>
