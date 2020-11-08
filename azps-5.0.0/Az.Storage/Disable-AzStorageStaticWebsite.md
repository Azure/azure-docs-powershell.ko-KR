---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: a7814734f33e0a68fefacf4e465c1834cce17708
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226078"
---
# <span data-ttu-id="1201b-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1201b-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="1201b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1201b-102">SYNOPSIS</span></span>
<span data-ttu-id="1201b-103">Azure 저장소 계정에 대 한 정적 웹 사이트를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1201b-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="1201b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1201b-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1201b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1201b-105">DESCRIPTION</span></span>
<span data-ttu-id="1201b-106">**AzStorageStaticWebsite** Cmdlet은 Azure 저장소 계정에 대 한 정적 웹 사이트를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1201b-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="1201b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1201b-107">EXAMPLES</span></span>

### <span data-ttu-id="1201b-108">예제 1: Azure 저장소 계정에 정적 웹 사이트 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="1201b-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="1201b-109">이 명령은 Azure 저장소 계정에 대 한 정적 웹 사이트를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1201b-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="1201b-110">변수</span><span class="sxs-lookup"><span data-stu-id="1201b-110">PARAMETERS</span></span>

### <span data-ttu-id="1201b-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="1201b-111">-Context</span></span>
<span data-ttu-id="1201b-112">Azure 저장소 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="1201b-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="1201b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1201b-113">-DefaultProfile</span></span>
<span data-ttu-id="1201b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1201b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1201b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1201b-115">-PassThru</span></span>
<span data-ttu-id="1201b-116">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="1201b-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1201b-117">-확인</span><span class="sxs-lookup"><span data-stu-id="1201b-117">-Confirm</span></span>
<span data-ttu-id="1201b-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1201b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1201b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1201b-119">-WhatIf</span></span>
<span data-ttu-id="1201b-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1201b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1201b-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1201b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1201b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1201b-122">CommonParameters</span></span>
<span data-ttu-id="1201b-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1201b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1201b-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1201b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1201b-125">입력</span><span class="sxs-lookup"><span data-stu-id="1201b-125">INPUTS</span></span>

### <span data-ttu-id="1201b-126">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1201b-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1201b-127">출력</span><span class="sxs-lookup"><span data-stu-id="1201b-127">OUTPUTS</span></span>

### <span data-ttu-id="1201b-128">WindowsAzure. ResourceModel를 PSStaticWebsiteProperties로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1201b-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="1201b-129">상속자</span><span class="sxs-lookup"><span data-stu-id="1201b-129">NOTES</span></span>

## <span data-ttu-id="1201b-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1201b-130">RELATED LINKS</span></span>
