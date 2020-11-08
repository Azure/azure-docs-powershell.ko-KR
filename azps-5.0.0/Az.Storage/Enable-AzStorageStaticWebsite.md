---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: e97e89c1ab7160f1eb06c9c94cd5620a48b0463e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216019"
---
# <span data-ttu-id="70efc-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="70efc-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="70efc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70efc-102">SYNOPSIS</span></span>
<span data-ttu-id="70efc-103">Azure 저장소 계정에 정적 웹 사이트를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70efc-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="70efc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70efc-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70efc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="70efc-105">DESCRIPTION</span></span>
<span data-ttu-id="70efc-106">**AzStorageStaticWebsite** Cmdlet은 Azure 저장소 계정에 대 한 정적 웹 사이트를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70efc-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="70efc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="70efc-107">EXAMPLES</span></span>

### <span data-ttu-id="70efc-108">예제 1: Azure 저장소 계정에 정적 웹 사이트 사용</span><span class="sxs-lookup"><span data-stu-id="70efc-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="70efc-109">이 명령은 Azure 저장소 계정에 대 한 정적 웹 사이트를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70efc-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="70efc-110">변수</span><span class="sxs-lookup"><span data-stu-id="70efc-110">PARAMETERS</span></span>

### <span data-ttu-id="70efc-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="70efc-111">-Context</span></span>
<span data-ttu-id="70efc-112">Azure 저장소 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="70efc-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="70efc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70efc-113">-DefaultProfile</span></span>
<span data-ttu-id="70efc-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70efc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70efc-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="70efc-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="70efc-116">404이 실행 될 때 표시 되어야 하는 오류 문서의 경로 (즉, 브라우저에서 존재 하지 않는 페이지를 요청 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="70efc-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

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

### <span data-ttu-id="70efc-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="70efc-117">-IndexDocument</span></span>
<span data-ttu-id="70efc-118">각 디렉터리의 인덱스 문서 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70efc-118">The name of the index document in each directory.</span></span>

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

### <span data-ttu-id="70efc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70efc-119">-PassThru</span></span>
<span data-ttu-id="70efc-120">ServiceProperties에서 정적 웹 사이트 설정을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="70efc-120">Display Static Website setting in ServiceProperties.</span></span>

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

### <span data-ttu-id="70efc-121">-확인</span><span class="sxs-lookup"><span data-stu-id="70efc-121">-Confirm</span></span>
<span data-ttu-id="70efc-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="70efc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70efc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70efc-123">-WhatIf</span></span>
<span data-ttu-id="70efc-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="70efc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70efc-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70efc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70efc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70efc-126">CommonParameters</span></span>
<span data-ttu-id="70efc-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70efc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70efc-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70efc-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70efc-129">입력</span><span class="sxs-lookup"><span data-stu-id="70efc-129">INPUTS</span></span>

### <span data-ttu-id="70efc-130">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="70efc-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="70efc-131">출력</span><span class="sxs-lookup"><span data-stu-id="70efc-131">OUTPUTS</span></span>

### <span data-ttu-id="70efc-132">WindowsAzure. ResourceModel를 PSStaticWebsiteProperties로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="70efc-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="70efc-133">상속자</span><span class="sxs-lookup"><span data-stu-id="70efc-133">NOTES</span></span>

## <span data-ttu-id="70efc-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70efc-134">RELATED LINKS</span></span>
