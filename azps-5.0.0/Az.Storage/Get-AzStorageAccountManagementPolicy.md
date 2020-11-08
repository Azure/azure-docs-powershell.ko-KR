---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: b27d6e8bec4dda2ba87a0b38a9b37a8d4739ae00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226478"
---
# <span data-ttu-id="080cf-101">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="080cf-101">Get-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="080cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="080cf-102">SYNOPSIS</span></span>
<span data-ttu-id="080cf-103">Azure 저장소 계정의 관리 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="080cf-103">Gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="080cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="080cf-104">SYNTAX</span></span>

### <span data-ttu-id="080cf-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="080cf-105">AccountName (Default)</span></span>
```
Get-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="080cf-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="080cf-106">AccountResourceId</span></span>
```
Get-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="080cf-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="080cf-107">AccountObject</span></span>
```
Get-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="080cf-108">설명은</span><span class="sxs-lookup"><span data-stu-id="080cf-108">DESCRIPTION</span></span>
<span data-ttu-id="080cf-109">**AzStorageAccountManagementPolicy** Cmdlet은 Azure 저장소 계정의 관리 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="080cf-109">The **Get-AzStorageAccountManagementPolicy** cmdlet gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="080cf-110">예제의</span><span class="sxs-lookup"><span data-stu-id="080cf-110">EXAMPLES</span></span>

### <span data-ttu-id="080cf-111">예제 1: 저장소 계정의 관리 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="080cf-111">Example 1: Get the management policy of a Storage account.</span></span>
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

<span data-ttu-id="080cf-112">이 명령은 저장소 계정의 관리 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="080cf-112">This command gets the management policy of a Storage account.</span></span>

## <span data-ttu-id="080cf-113">변수</span><span class="sxs-lookup"><span data-stu-id="080cf-113">PARAMETERS</span></span>

### <span data-ttu-id="080cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="080cf-114">-DefaultProfile</span></span>
<span data-ttu-id="080cf-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="080cf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="080cf-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="080cf-116">-ResourceGroupName</span></span>
<span data-ttu-id="080cf-117">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="080cf-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="080cf-118">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="080cf-118">-StorageAccount</span></span>
<span data-ttu-id="080cf-119">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="080cf-119">Storage account object</span></span>

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

### <span data-ttu-id="080cf-120">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="080cf-120">-StorageAccountName</span></span>
<span data-ttu-id="080cf-121">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="080cf-121">Storage Account Name.</span></span>

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

### <span data-ttu-id="080cf-122">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="080cf-122">-StorageAccountResourceId</span></span>
<span data-ttu-id="080cf-123">저장소 계정 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="080cf-123">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="080cf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="080cf-124">CommonParameters</span></span>
<span data-ttu-id="080cf-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="080cf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="080cf-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="080cf-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="080cf-127">입력</span><span class="sxs-lookup"><span data-stu-id="080cf-127">INPUTS</span></span>

### <span data-ttu-id="080cf-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="080cf-128">System.String</span></span>

## <span data-ttu-id="080cf-129">출력</span><span class="sxs-lookup"><span data-stu-id="080cf-129">OUTPUTS</span></span>

### <span data-ttu-id="080cf-130">StorageAccountKey를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="080cf-130">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="080cf-131">상속자</span><span class="sxs-lookup"><span data-stu-id="080cf-131">NOTES</span></span>

## <span data-ttu-id="080cf-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="080cf-132">RELATED LINKS</span></span>
