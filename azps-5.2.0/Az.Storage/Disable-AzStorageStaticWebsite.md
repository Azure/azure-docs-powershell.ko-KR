---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: a7814734f33e0a68fefacf4e465c1834cce17708
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349802"
---
# <span data-ttu-id="ed1c3-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ed1c3-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="ed1c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed1c3-102">SYNOPSIS</span></span>
<span data-ttu-id="ed1c3-103">Azure Storage 계정에 대한 정적 웹 사이트를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="ed1c3-104">구문</span><span class="sxs-lookup"><span data-stu-id="ed1c3-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed1c3-105">설명</span><span class="sxs-lookup"><span data-stu-id="ed1c3-105">DESCRIPTION</span></span>
<span data-ttu-id="ed1c3-106">**Disable-AzStorageStaticWebsite** cmdlet은 Azure Storage 계정에 대한 정적 웹 사이트를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="ed1c3-107">예제</span><span class="sxs-lookup"><span data-stu-id="ed1c3-107">EXAMPLES</span></span>

### <span data-ttu-id="ed1c3-108">예제 1: Azure Storage 계정에 대한 정적 웹 사이트 비활성화</span><span class="sxs-lookup"><span data-stu-id="ed1c3-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="ed1c3-109">이 명령은 Azure Storage 계정에 대한 정적 웹 사이트를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="ed1c3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed1c3-110">PARAMETERS</span></span>

### <span data-ttu-id="ed1c3-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ed1c3-111">-Context</span></span>
<span data-ttu-id="ed1c3-112">Azure Storage 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="ed1c3-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="ed1c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed1c3-113">-DefaultProfile</span></span>
<span data-ttu-id="ed1c3-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed1c3-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed1c3-115">-PassThru</span></span>
<span data-ttu-id="ed1c3-116">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="ed1c3-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ed1c3-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed1c3-117">-Confirm</span></span>
<span data-ttu-id="ed1c3-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed1c3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed1c3-119">-WhatIf</span></span>
<span data-ttu-id="ed1c3-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ed1c3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed1c3-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed1c3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed1c3-122">CommonParameters</span></span>
<span data-ttu-id="ed1c3-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed1c3-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed1c3-125">입력</span><span class="sxs-lookup"><span data-stu-id="ed1c3-125">INPUTS</span></span>

### <span data-ttu-id="ed1c3-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ed1c3-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ed1c3-127">출력</span><span class="sxs-lookup"><span data-stu-id="ed1c3-127">OUTPUTS</span></span>

### <span data-ttu-id="ed1c3-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="ed1c3-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="ed1c3-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ed1c3-129">NOTES</span></span>

## <span data-ttu-id="ed1c3-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed1c3-130">RELATED LINKS</span></span>