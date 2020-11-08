---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: c8a32cb86ace86cb0f2775db98f49f57408be6f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216354"
---
# <span data-ttu-id="b2f22-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b2f22-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="b2f22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2f22-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f22-103">Azure 저장소 Blob 서비스에 대해 보존 정책 삭제를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f22-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="b2f22-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b2f22-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2f22-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b2f22-105">DESCRIPTION</span></span>
<span data-ttu-id="b2f22-106">**AzStorageDeleteRetentionPolicy** Cmdlet은 Azure Storage Blob service에 대 한 삭제 보존 정책을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f22-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="b2f22-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b2f22-107">EXAMPLES</span></span>

### <span data-ttu-id="b2f22-108">예제 1: Blob 서비스에 대 한 삭제 보존 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="b2f22-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="b2f22-109">이 명령은 Blob 서비스에 대 한 삭제 보존 정책을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f22-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="b2f22-110">변수</span><span class="sxs-lookup"><span data-stu-id="b2f22-110">PARAMETERS</span></span>

### <span data-ttu-id="b2f22-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="b2f22-111">-Context</span></span>
<span data-ttu-id="b2f22-112">Azure 저장소 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="b2f22-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="b2f22-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2f22-113">-DefaultProfile</span></span>
<span data-ttu-id="b2f22-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2f22-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2f22-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2f22-115">-PassThru</span></span>
<span data-ttu-id="b2f22-116">DeleteRetentionPolicyProperties 표시</span><span class="sxs-lookup"><span data-stu-id="b2f22-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="b2f22-117">-확인</span><span class="sxs-lookup"><span data-stu-id="b2f22-117">-Confirm</span></span>
<span data-ttu-id="b2f22-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f22-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2f22-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2f22-119">-WhatIf</span></span>
<span data-ttu-id="b2f22-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b2f22-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2f22-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2f22-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2f22-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f22-122">CommonParameters</span></span>
<span data-ttu-id="b2f22-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f22-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f22-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2f22-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f22-125">입력</span><span class="sxs-lookup"><span data-stu-id="b2f22-125">INPUTS</span></span>

### <span data-ttu-id="b2f22-126">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b2f22-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b2f22-127">출력</span><span class="sxs-lookup"><span data-stu-id="b2f22-127">OUTPUTS</span></span>

### <span data-ttu-id="b2f22-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b2f22-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="b2f22-129">상속자</span><span class="sxs-lookup"><span data-stu-id="b2f22-129">NOTES</span></span>

## <span data-ttu-id="b2f22-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2f22-130">RELATED LINKS</span></span>
