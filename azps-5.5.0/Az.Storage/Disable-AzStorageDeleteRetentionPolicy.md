---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: c8a32cb86ace86cb0f2775db98f49f57408be6f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190913"
---
# <span data-ttu-id="72830-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="72830-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="72830-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72830-102">SYNOPSIS</span></span>
<span data-ttu-id="72830-103">Azure Storage Blob service에 대한 삭제 보존 정책을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="72830-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="72830-104">구문</span><span class="sxs-lookup"><span data-stu-id="72830-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72830-105">설명</span><span class="sxs-lookup"><span data-stu-id="72830-105">DESCRIPTION</span></span>
<span data-ttu-id="72830-106">**Disable-AzStorageDeleteRetentionPolicy** cmdlet은 Azure Storage Blob service에 대한 삭제 보존 정책을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="72830-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="72830-107">예제</span><span class="sxs-lookup"><span data-stu-id="72830-107">EXAMPLES</span></span>

### <span data-ttu-id="72830-108">예제 1: Blob service에 대한 삭제 보존 정책 사용 안</span><span class="sxs-lookup"><span data-stu-id="72830-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="72830-109">이 명령은 Blob service에 대한 삭제 보존 정책을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="72830-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="72830-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72830-110">PARAMETERS</span></span>

### <span data-ttu-id="72830-111">-Context</span><span class="sxs-lookup"><span data-stu-id="72830-111">-Context</span></span>
<span data-ttu-id="72830-112">Azure Storage 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="72830-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="72830-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72830-113">-DefaultProfile</span></span>
<span data-ttu-id="72830-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="72830-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72830-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72830-115">-PassThru</span></span>
<span data-ttu-id="72830-116">DeleteRetentionPolicyProperties 표시</span><span class="sxs-lookup"><span data-stu-id="72830-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="72830-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72830-117">-Confirm</span></span>
<span data-ttu-id="72830-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="72830-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72830-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72830-119">-WhatIf</span></span>
<span data-ttu-id="72830-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="72830-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72830-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72830-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72830-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72830-122">CommonParameters</span></span>
<span data-ttu-id="72830-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="72830-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72830-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="72830-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72830-125">입력</span><span class="sxs-lookup"><span data-stu-id="72830-125">INPUTS</span></span>

### <span data-ttu-id="72830-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="72830-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="72830-127">출력</span><span class="sxs-lookup"><span data-stu-id="72830-127">OUTPUTS</span></span>

### <span data-ttu-id="72830-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="72830-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="72830-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="72830-129">NOTES</span></span>

## <span data-ttu-id="72830-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="72830-130">RELATED LINKS</span></span>
