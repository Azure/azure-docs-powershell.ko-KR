---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/get-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: f19aaf41a7f2874e0d32df3dddec3f0b8fcb6779
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002795"
---
# <span data-ttu-id="55abc-101">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="55abc-101">Get-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="55abc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55abc-102">SYNOPSIS</span></span>
<span data-ttu-id="55abc-103">Azure Storage 계정의 관리 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="55abc-103">Gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="55abc-104">구문</span><span class="sxs-lookup"><span data-stu-id="55abc-104">SYNTAX</span></span>

### <span data-ttu-id="55abc-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="55abc-105">AccountName (Default)</span></span>
```
Get-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55abc-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="55abc-106">AccountResourceId</span></span>
```
Get-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55abc-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="55abc-107">AccountObject</span></span>
```
Get-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55abc-108">설명</span><span class="sxs-lookup"><span data-stu-id="55abc-108">DESCRIPTION</span></span>
<span data-ttu-id="55abc-109">**Get-AzStorageAccountManagementPolicy** cmdlet은 Azure Storage 계정의 관리 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="55abc-109">The **Get-AzStorageAccountManagementPolicy** cmdlet gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="55abc-110">예제</span><span class="sxs-lookup"><span data-stu-id="55abc-110">EXAMPLES</span></span>

### <span data-ttu-id="55abc-111">예제 1: Storage 계정의 관리 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="55abc-111">Example 1: Get the management policy of a Storage account.</span></span>
```
PS C:\>Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 7:04:05 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterModificationGreaterThan":  30
                                                                                                },
                                                                                 "TierToArchive":  {
                                                                                                       "DaysAfterModificationGreaterThan":  50
                                                                                                   },
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  {
                                                                                 "Delete":  {
                                                                                                "DaysAfterCreationGreaterThan":  100
                                                                                            }
                                                                             }
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  [
                                                                                    "prefix1",
                                                                                    "prefix2"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  true,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  null,
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="55abc-112">이 명령은 Storage 계정의 관리 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="55abc-112">This command gets the management policy of a Storage account.</span></span>

## <span data-ttu-id="55abc-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="55abc-113">PARAMETERS</span></span>

### <span data-ttu-id="55abc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55abc-114">-DefaultProfile</span></span>
<span data-ttu-id="55abc-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55abc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55abc-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55abc-116">-ResourceGroupName</span></span>
<span data-ttu-id="55abc-117">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55abc-117">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55abc-118">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="55abc-118">-StorageAccount</span></span>
<span data-ttu-id="55abc-119">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="55abc-119">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55abc-120">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="55abc-120">-StorageAccountName</span></span>
<span data-ttu-id="55abc-121">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55abc-121">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55abc-122">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="55abc-122">-StorageAccountResourceId</span></span>
<span data-ttu-id="55abc-123">Storage 계정 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="55abc-123">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55abc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55abc-124">CommonParameters</span></span>
<span data-ttu-id="55abc-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="55abc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55abc-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="55abc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55abc-127">입력</span><span class="sxs-lookup"><span data-stu-id="55abc-127">INPUTS</span></span>

### <span data-ttu-id="55abc-128">System.String</span><span class="sxs-lookup"><span data-stu-id="55abc-128">System.String</span></span>

## <span data-ttu-id="55abc-129">출력</span><span class="sxs-lookup"><span data-stu-id="55abc-129">OUTPUTS</span></span>

### <span data-ttu-id="55abc-130">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="55abc-130">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="55abc-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="55abc-131">NOTES</span></span>

## <span data-ttu-id="55abc-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55abc-132">RELATED LINKS</span></span>
