---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: e97e89c1ab7160f1eb06c9c94cd5620a48b0463e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198492"
---
# <span data-ttu-id="82cb8-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="82cb8-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="82cb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="82cb8-103">Azure Storage 계정에 대해 정적 웹 사이트를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="82cb8-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="82cb8-104">구문</span><span class="sxs-lookup"><span data-stu-id="82cb8-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82cb8-105">설명</span><span class="sxs-lookup"><span data-stu-id="82cb8-105">DESCRIPTION</span></span>
<span data-ttu-id="82cb8-106">**Enable-AzStorageStaticWebsite** cmdlet을 사용하면 Azure Storage 계정에 대한 정적 웹 사이트를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82cb8-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="82cb8-107">예제</span><span class="sxs-lookup"><span data-stu-id="82cb8-107">EXAMPLES</span></span>

### <span data-ttu-id="82cb8-108">예제 1: Azure Storage 계정에 대해 정적 웹 사이트 사용</span><span class="sxs-lookup"><span data-stu-id="82cb8-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="82cb8-109">이 명령은 Azure Storage 계정에 대한 정적 웹 사이트를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82cb8-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="82cb8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82cb8-110">PARAMETERS</span></span>

### <span data-ttu-id="82cb8-111">-Context</span><span class="sxs-lookup"><span data-stu-id="82cb8-111">-Context</span></span>
<span data-ttu-id="82cb8-112">Azure Storage 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="82cb8-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="82cb8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82cb8-113">-DefaultProfile</span></span>
<span data-ttu-id="82cb8-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82cb8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82cb8-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="82cb8-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="82cb8-116">404가 발급될 때 표시해야 하는 오류 문서의 경로입니다(브라우저에서 존재하지 않는 페이지를 요청하는 경우).</span><span class="sxs-lookup"><span data-stu-id="82cb8-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cb8-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="82cb8-117">-IndexDocument</span></span>
<span data-ttu-id="82cb8-118">각 디렉터리의 인덱스 문서 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82cb8-118">The name of the index document in each directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cb8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82cb8-119">-PassThru</span></span>
<span data-ttu-id="82cb8-120">ServiceProperties에서 정적 웹 사이트 설정을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="82cb8-120">Display Static Website setting in ServiceProperties.</span></span>

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

### <span data-ttu-id="82cb8-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82cb8-121">-Confirm</span></span>
<span data-ttu-id="82cb8-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="82cb8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82cb8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82cb8-123">-WhatIf</span></span>
<span data-ttu-id="82cb8-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="82cb8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82cb8-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82cb8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82cb8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82cb8-126">CommonParameters</span></span>
<span data-ttu-id="82cb8-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82cb8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82cb8-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="82cb8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82cb8-129">입력</span><span class="sxs-lookup"><span data-stu-id="82cb8-129">INPUTS</span></span>

### <span data-ttu-id="82cb8-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="82cb8-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="82cb8-131">출력</span><span class="sxs-lookup"><span data-stu-id="82cb8-131">OUTPUTS</span></span>

### <span data-ttu-id="82cb8-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="82cb8-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="82cb8-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82cb8-133">NOTES</span></span>

## <span data-ttu-id="82cb8-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82cb8-134">RELATED LINKS</span></span>
